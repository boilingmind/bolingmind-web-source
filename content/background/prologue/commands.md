---
title: "Implementation"
description: "Doks comes with commands for common tasks."
lead: "Doks comes with commands for common tasks."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu: 
  docs:
    parent: "background"
weight: 130
toc: true
---

The collected physiological data of the audience is transmitted to the server over WiFi. The server re-streams the processed data to other computers controlling each staging element. 


## Sensing Electrodermal and Heart Activity of the Audience

For this project we built wrist-worn devices measuring EDA from 2 electrodes on the fingers, and the heart rate using an optical blood volume pulse sensor. EDA signal was sampled at 4.545 Hz and the heart rate sensor at 50Hz.
The recorded data was buffered in 400ms chunks and streamed to the server 2.5 times per second. The device was built around the ESP32 module with Bluetooth and WiFi connectivity. Internally the device samples the blood volume pulse at 500 Hz and runs heart beat detection on the 500 Hz data. Every 10th sample (50Hz), beats per minute and inter-beat interval were streamed to the server. EDA is sampled at 4.545 Hz, is digitally filtered and sent to the server as well, both raw values for recording and further analysis, and filtered values for visualisations. Transient response time of the filter output is guaranteed to be within 5\% of the steady state in 10 seconds, this is necessary to provide smooth signal for the visuals generation without the noise from touching or adjusting the electrodes. In order to save energy, each device is buffering all the data in every 400ms window and sends out the buffer 2.5 times per second.
The server software was recording and re-streaming the data to other machines used for staging controls . Stress tests showed that our system could handle up to 60 devices using a Netgear Nighthawk series WiFi router. Calculation of the HRV parameters such as LF/HF ratio was done on the server side. The aggregated and processed data was sent out to other machines in OSC format over UDP protocol via an Ethernet link.


%In order to maintain the 50 Hz data rate, the server was buffering the stream from each device and gradually FIFO de-buffering it. To smooth out the possible network delays without sacrificing the quality of the visualisations, the server was gradually reducing or increasing the OSC stream rate if there was less than 300ms or more than 500ms of data buffered. The delay between a data sample originating on a device and its effect on the visuals was averaging to about 400-500ms.

## Visualizations

We projected the visualizations rendered based on the audience physiological responses. Since the projection was covering the whole stage, it played a significant role in setting the mood and atmosphere. In the design process of the visualisations we had the following considerations and requirements:


* Visualisations should reflect audiences' physiological reactions in real-time.
* Visualisations have to be easy to understand by both audience and dancers at a glance.
* Visualisations have to reflect the atmosphere, tone and story of each scene.



Visualisations were rendered and projected onto the stage using [TouchDesigner]{https://derivative.ca} software. We used 3 projectors so that the visualizations could cover the whole space. We based the visual design around an intuitively comprehensible color scheme. A number of studies indicate that individuals tend to associate red colors with arousal and excitation whereas blue colors are associated with quietness and relaxation. Therefore, in our design we used warm colors such as red to represent arousal and cold colors such as blue to represent relaxation. The LF/HF ratio was mapped to the blue and red extremes of a gradient as shown in Figure \ref{fig:MappingHFLFandColors}. The predominant color of the visualisations changed according to either the real-time average LF/HF ratio of the whole audience or one particular spectator's data. 

%We designed multiple types of visuals using this color mapping, such as one that changes according to the real-time average HF/LF ratio of all the audience members, or one that focuses on a particular audience member and visualizes the HF/LF ratio.

The EDA signal was mapped to the visuals as well. EDA signal interpretation concentrates on the rate of change rather than the absolute values. For each visualization, the rate of change of the EDA signal affected the visualizations' movement speed. That is, the faster the EDA changed, the more intense the movement of the visualizations became. As a result, the audience and the dancers may understand the extent of the audience reaction from the movement of the visualization. 



## Audio
The audio setup for this work consisted of 11 speakers: 9 small mono speakers placed on the ceiling, and two large speakers on the floor at the back of the stage. The small speakers on the ceiling were used primarily for supplemental sound design.%, such as manipulated recordings of the dancers stomping in their high heels. 


These sounds were faded in along with excitement levels of the audience. We decided upon this approach as a way to not only allow the audience data to guide another aspect of the performance, but also to give the dancers a sonic cue of how engaged the audience was during these moments. The upper speakers were also responsible for projecting additional timbral layers in several scenes. Overall, the disbursement of the cumulative soundscapes was divided up with roughly three-quarters of the audio layers assigned to the main speakers and the remaining quarter of the audio layers assigned to the ceiling speakers. This was decided after conducting several trials, in which this balance between consistent audio and supplemental/reactive audio was found to be strongest for the production team and the performers.%with roughly 75\% of the sound coming from the main speakers, with the remaining 25\% from the ceiling. This added a more immersive sonic experience while also creating a slight divide between the structural music and the supplemental data-driven sound design.

# Lighting 
The interactive lighting system consisted of 6 moving head lights on two axes placed around the stage. There were 2 light modes: mode 1 was used in several scenes, while mode 2 was used during one of the performance scenes.
In the first mode, 6 members from the audience were selected with their HR data mapped to the intensity of the corresponding light. When more than one person had similar beats per minute (BPM) rate, they would be considered as a group.

The lights corresponding to this group would move to point at each other. When someone's BPM changed to a different value from the rest of the group, the corresponding light would move back to its initial position. The light would then be re-assigned to a different member.

Once a mode was switched on, the lighting can function automatically until switched to a different mode. 
Thus, the lighting design complements the visualization of the audience as a group or as an individual. In addition, it also affected the dancers by highlighting the inner states of the audience through brightness levels and lighting movements. 



