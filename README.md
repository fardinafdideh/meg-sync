![](ppt/logos.png)

# ⏱️ Synchronization in Multi-PC MEG Setups
![MEG](https://img.shields.io/badge/Tools-MEG%20%7C%20EyeLink%20%7C%20Psychtoolbox%20%7C%20Photodiode-orange.svg)

This research work was supported by ERC project [BrainDyn](https://cordis.europa.eu/project/id/716862) (PI: Dr. [Mathilde Bonnefond](https://scholar.google.com/citations?user=Xc1fz38AAAAJ&hl=en)).

## 📖 Overview
In complex Magnetoencephalography (MEG) experiments, precise temporal alignment is critical. 
This work characterizes and optimizes the timing synchrony between multiple subsystems: the Controller PC, MEG Acquisition PC, and Eye-Tracking (Eyelink) PC.
The project addresses a fundamental research question: How precise is signal synchronization between different PCs, and can this precision be improved?

## ⚙️ Pipeline
The following workflow illustrates the hardware communication and the trigger markers analyzed to measure latency and drift.

![](ppt/Slide3.PNG)
```mermaid
graph TD
    subgraph "MEG Stream"
      MEGPC --> STORAGE_MEG[(MEG Storage)]
    end

    subgraph "Stimulus Stream"
      stim[Stimulation Screen] -- Light Intensity --> PD[Photodiode]
      PD --> MEGPC
    end

    subgraph "Eye Tracker Stream"
        EL[Eyelink PC] --> STORAGE_EL[(EDF Storage)]
    end

    CPC[Controller PC] --VBL--> stim
    CPC --"TTL Trigger (io64)"--> MEGPC[MEG PC]
    CPC --"TTL Trigger (io64)"--> EL
```

## 🔬 Synchronization in Multi-PC MEG Setups
![](ppt/Slide1.PNG)
![](ppt/Slide2.PNG)
![](ppt/Slide3.PNG)
![](ppt/Slide4.PNG)
![](ppt/Slide5.PNG)
![](ppt/Slide6.PNG)
![](ppt/Slide7.PNG)
![](ppt/Slide8.PNG)
![](ppt/Slide9.PNG)
![](ppt/Slide10.PNG)
![](ppt/Slide11.PNG)
![](ppt/Slide12.PNG)
![](ppt/Slide13.PNG)
![](ppt/Slide14.PNG)
![](ppt/Slide15.PNG)
![](ppt/Slide16.PNG)

## 📚 How to cite
* F. Afdideh et al., "Timing and Synchronisation Between Different PCs in an MEG Setup", unpublished.
