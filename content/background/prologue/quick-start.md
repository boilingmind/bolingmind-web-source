---
title: "Perfromance Details"
description: "One page summary of how to start a new Doks project."
lead: "One page summary of how to start a new Doks project."
date: 2020-11-16T13:59:39+01:00
lastmod: 2020-11-16T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "background"
weight: 110
toc: true
---

## Requirements

In March 2020 we conducted three performances. The performances were advertised mentioning that we will be using the physiological signals and a brief introduction of what would be expected to happen during the performance. All the audience members were asked to read through the consent form on their seats (See Fig.\ref{fig:wrist} Left). By signing the form, they agreed to participate in this work and to offer their physiological data.  
The performance, including the data streaming and recording, was conducted according to the ethics rules and regulations of the ethics board of {\bf university blinded for review}.

Each live performance lasted for about 1 hour and involved 7 dancers enacting the scenes. 

### a- Introduction (5 minutes)

Before the performance started, we introduced the design of the stage elements and physiological sensing to the audience to explain how the stage elements would change depending on their physiological responses. We explained how sensors impact the discrete parts of the performances with raw data and stage element examples. We also emphasized the informed consent regarding the sensor data, explaining the kind of data and potential risks with EDA/heartrate recordings. Some audience members could not wear the sensors or decide not to be recorded. 
As the audience members were informed over flyers and brochures beforehand about the recording, 
only few opted out completely. The audience members could see raw data and several visualizations based on an individual volunteer and aggregates.
%The stage elements were kept straightforward and easy to understand in order to keep the audience interested and excited about the performance. 
%the explanation text was projected onto the stage while 2 presenters repeated the explanation orally. On the right side we demonstrated how the visuals change in response to changes in HF/LF ratio and EDA. 


### b- Business Card Scene (3 minutes)
The performance starts from Ravel's classical piece Boléro. Shortly after the beginning, the 7 dancers blend into the audience and talk to audience members while handing them their own business cards. The physiological data from the audience members of this scene was plotted individually in the form of a real-time graph, with all the audience's graphs displayed side-by-side as shown in Figure \ref{fig:TypesOfVisuals}(b). Each graph contained the heart rate waveform, BPM, LF/HF ratio value, EDA value, and ID of the spectator. The audience was able to see visualizations of their own data reflecting on the stage.As a result of initial tests, many audience members expressed a desire to see how their biometric information changed while watching the dance performance. The act of watching a dance is a very personal experience for the audience, and they are desperate to find common ground between their own experience and what happens on stage. To assist the audience in this quest, we designed the piece to visualize each audience member's biometric information as the key to connecting the audience and the stage. As the emotional response of those who received business cards from dancers spiked drastically, it was also clearly visible in the graphs. 
%the dance performance starts in earnest.
% compare their own emotions with the graph on the stage and

### c- Boléro (15 minutes)
As Boléro continued to build up, the dancers started moving slowly and quietly, wearing suits and high heels. They gradually took them off and exploded in sync with the rhythm and crescendo of Boléro. 
%This intense movement was designed to raise the excitement level of the audience, mirroring the rhythmic and dynamic crescendo of Boléro.
As the rhythm of Boléro and the rhythm of the high heels hitting the floor synchronized, the visualization changed to a more abstract representation.
In this scene, each spectator's data was transformed into an orb that changed color depending on the respective LF/HF value. The shape of this orb was indeterminate, and the speed of its movement depended on the EDA signal changes. Also, Mode1 was used for lighting. %In other words, the orb of a audience with a high HF/LF ratio and a steep EDA value is more red and shakes more violently.

### d- Ghostly Amenities (10 minutes):

Each performer danced with a puppet that represented their alter ego. In the end, the dancers handed the puppet to an audience member. The choreography and music set a mysterious tone in this scene. The visuals were designed to amplify this tone. We used a fluid simulation and created a smoke-filled space. The amount and frequency of appearance of the smoke clouds was varied by means of the LF/HF value. The mean of the EDA values also affected the parameters of the fluid simulation of the smoke. When the EDA data from the audience suggested sedation, there was less smoke, and vice versa (See Figure \ref{fig:TypesOfVisuals}(d)).
\\The musical score consisted of four movements which were separated and played back depending on the pacing of the choreography. The physiological data from the audience was used as a graphic score guiding the implementation of reverb and a low pass filter (LPF). As the excitement levels increased, the LPF allowed more sub-frequencies into the soundscape. This design was intended to further increase the excitement levels due to the physical nature of the low frequencies, while the reverb was used as an auditory cue for the changes occurring.

### e- Romeo (15 minutes):
One dancer spoke the line, "If I see your mind, I will dance with it". The phrase and idea came from the lighting technician during discussions leading to the artistic decision to include a more directly linked performance between dancer and audience member. Next, a different dancer picked an audience member and invited him to the stage to play the role of her Romeo. The dancer chose a male spectator from the first row at their own discretion. The spectator needed to have an active sensor and consented to the public data use.
 
In this scene, the visualization showed the LF/HF and EDA plot, except the data used was picked up from the chosen Romeo. For all three performances, the LF/HF ratio of the Romeo indicated a high level of excitement. For this scene, we linked all the lights to the Romeo audience member using Mode2 lighting.

The dancers could perceive the emotional state of the chosen Romeo based on the color of the visual projection. When it turned red, the dancers would start to improvise and reach out to Romeo, as if saying they were happy to see him here. If he smiled, the dancers would dance with him in a playful way.

### f- Chaos (5 minutes) 
This scene described the conflicting and complex feelings of instability, confusion, and joy that we all experience as we grow from childhood to adulthood. The visualization moved in the form of a wave, with the average LF/HF value changing the color of the wave, and the average EDA value changing the height of the wave as shown as Figure \ref{fig:TypesOfVisuals}(f). Also, Mode1 was used for lighting.
%In this scene, the average data of the audience was used to change the visualization,
%to express the emotional trend of the audience at the halfway point of the performance. 
\\
The score for this movement began with a looping drum beat which was then manipulated based on the physiological data. The EDA levels would trigger a stuttering effect which was played back through the ceiling speakers. The LF/HF values dictated the pitch variance in the drum sounds. Lastly, the movements of the solo performer dictated the duration of the drum solo and the entrance of the subsequent synthesizer passages. Solo dancers improvised to the rhythm of the audience's interlocking LF/HF ratio. As the audience's excitement level increased, the music became disjointed, forcing the dancers to move with unnatural pauses and a complex juxtaposition of tension and relaxation.

### g- Loving Animal Companion (15 minutes)
One dancer followed another dancer like a playful animal companion (e.g. dog) willingly walking after its owner, clinging to her legs.
In this scene, we used particle colors linked to the LF/HF values and particle density linked to EDA as shown in Figure \ref{fig:TypesOfVisuals}(g). The particle effect was rendered to illustrate the change from red to blue as the audience was more sedated, mirroring the slow choreography and aesthetic tone.
 %we varied the visualization according to the average HF/LF and EDA values of the audience. 
 
The music for this scene was also quite sedated and relaxed. The musical director used the incoming data to guide when various musical layers would enter and exit. In addition to these musical layers, heavily manipulated sounds of high heels were played back through the ceiling speakers as a reference to the earlier parts of the performance. These heel sounds were faded in and out based on the LF/HF and EDA levels. 

In fact, the audience was sedate and the visuals and music were always calmingly staged, so that the dancers were immersed in choreography that evoked a sense of security and trust, which was the original purpose of the performance.

### h- Ending (10 minutes)
The music and choreography of the final scene was a reference to the first Boléro scene. The visual design was also the same as in the business card and Boléro scenes.
The similarity and references between the ending scene and the beginning scene are purposely delivered to the audience so that they can compare the different states they perceived with the visualization before and after experiencing the entire performance. 

To sum up, Boiling Mind was a one-hour contemporary dance performance based on "Boléro" composed by Maurice Ravel. The choreography in Boiling Mind incorporated the mechanism of interpersonal synchrony to create a feedback loop between the audience and the dancers. This was accomplished by sharing rhythms between interpersonal actors in a biosensor-based reactive performance.
%For example, when dancers hit their high heels against the floor in sync with Boléro's repetitive rhythms, we expected the audience to be more evoked and synchronize with the dancers and music, eliciting different arousal feelings.%Below is the detailed description of each performance scene:
57 people attended the first performance, 37 the second, and 45 the third performance. For the 3 performances, we had physiological data related to the emotional responses of 40, 35 and 40 members of the audience used in each respective performance. 



