# Archbook Project:

The project mainly aims to implement most of the functionality in KDE settings (https://userbase.kde.org/System_Settings) and extends it with device specific functionality. 

## Project Plan

![project_plan.png](/home/joe/Development/rust/archbook-project/project_plan.png)

## archbookd:

### archbookd_lib:

Provides functions to control computer as root

- Run shutdown commands (cmd and internal) 

- Run startup commands (cmd and internal)

- Peripheral Control:
  
  - Keyboard Control:
    
    - Change language/layout
    
    - Toggle on/off
    
    - Map keys (xbindkeys) 
    
    - Control Brightness
  
  - Mouse Control:
    
    - Toggle on/off
    
    - Map keys
    
    - Map Motions 
  
  - Touch pad Control:
    
    - Toggle on/off
    
    - Motions
  
  - Camera:
    
    - Toggle On/Off
    
    - Virtual Camera Control (v4l2loopback)
  
  - Microphone:
    
    - Toggle on/off

- Display Control:
  
  - Toggle touch on/off
  
  - Map touch screens
  
  - Toggle touch screens
  
  - Screenpad:
    
    - Toggle on/off by setting Brightness to 0
    
    - Toggle Dim by setting xrandr brightness to 0.1
    
    - Control Brightness 
  
  - Main Display:
    
    - Control Brightness 

- Hybrid Gpu control:
  
  - Enable integrated graphics card only
  
  - Enable dedicated graphics card only
  
  - hybrid use both

- CPU control:
  
  - Set CPU power mode vie Intel Hardware P-state (HWP)  
  
  - see: https://wiki.archlinux.org/title/CPU_frequency_scaling 

- Fan Control:
  
  - See: https://github.com/nbfc-linux/nbfc-linux/

- Power:
  
  - interact with power profiles daemon
  
  - set battery charge threshold 
  
  - set critical battery level and action
  
  - set action when idle for duration 

- Audio Control:
  
  - increase sink volume
  
  - decrease sink volume
  
  - mute microphone 

- Misc:
  
  - Plymouth startup/shutdown

### archbookd_daemon