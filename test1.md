# test cooling of "Raspberry_Cube" case
## 27.10.2019 23:21
#### reference: f8ff9a73f449049f0244390ff263996b0694c69f  Screencast_27.10.2019_23:21:28.mp4
3D printable Case for Raspberry Pi 3B+ **Cluster** 

1. test **scenario**
  - 2 raspberry Pi 3B+ running in cube, headless named **RC1** & **RC2**
  - powered by 4 port 16 Watt USB power supply device (5.1V with max sum current 3.1A) 
  - 30mm fan running with 5V
  - environment temperature ca. 20 GradC
  - remote login to both Pi's via ssh and tmux
  - 2 nearly identical screens with panes for 
      online temp logging, voltages, top, start of load, ...

2. test procedure
  - start of sysbench on each pi's nearly simultan
  - run time of sysbench for 10 minutes (600 secs)
  - switching between screens to control voltage, temp and freq.

3. main results
  - after idle running for some minutes, the temperature started at ca. **26.8 Grad C** on each Pi
  - start full load with sysbench for 10 minutes
  - max temperature reached below **43 Grad C** on each Pi
  - no throttling of cpu/gpu freq seen...

4. rough progress of RC2, (RC1 quiete similar)
  - 30 Grad C	4 sec
  - 32 Grad C	6 sec
  - 34 Grad C	13 sec
  - 36 Grad C	26 sec
  - 38 Grad C	38 sec
  - 40 Grad C	78 sec  1:18 min
  - 41 Grad C	146 sec	2:26 min
  - 42 Grad C	304 sec	4:24 min

## used "Cube" case
<img heigth="600" src="../master/pics/FrontLeftView.jpg" alt="cube_fl"/>
<img heigth="600" src="../master/pics/SideRightView.jpg" alt="cube_sr"/>
<img heigth="600" src="../master/pics/BackSideView.jpg" alt="cube_bs"/>
