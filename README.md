# Log data from Campbell scientific weather station
Program author: Jan Knappe,
Contact: [jan.knappe@tcd.ie](jan.knappe@tcd.ie),
Logger type: CR1000 (Campbell Scientific)

## Connected devices
Logger program to measure 
- Battery Voltage (V_batt) 
- Panel Temperature (T_panel)
- Case Temperature (T_case) on type T thermocouple
- Air Temperature (T_air as CS215out(1)) on CS215 
- Relative Humidity (RH as CS215out(2)) on CS215 
- Barometric Pressure (Pres) on CS106
- Rainfall (Rain) on ARG100
- Wind Speed (Wind_Spe) on 05103-5
- Wind Direction (Wind_Dir) on 05103-5
- Net Radiation (Rad_Net) on NR-2 Lite
- Pulses for tipping buckets distribution boxes (2x) on C6 and C8
- Volatge for VWC on 48x EC5 sensor at multiplexer 1
- Voltage for VWC on 33x EC5 sensor at multiplexer 2
- Permittivity (e) for VWC on 4x GS3 sensor at C5 port
- Electrical Conductivity (EC) on 4x GS3 sensor at C5 port
- Soil Temperature (T_soil) on 4x GS3 sensor at C5 port
  
## Sensor wiring
CR1000 - Thermocouple type T
8H - Blue
8L - Red
	
CR1000 - CS106 Barometric pressure sensor	
4H - Blue
AG - Yellow
G - Clear
G - Black
12V - Red
C4 - Green  

CR1000 - CS215 T+RH sensor via connector 1 (6 pin)
Ground - Clear
G - White
G - Black
12V - Red
C7 - Green
SDI-12 address: 9
  
CR1000 - 05103-5 Wind monitor via connector 2 (6 pin)
4L - Green
G - Black
G - Blue
G - White
VX2 - Blue 
P1 - Red 
 
CR1000 - NR-2 Lite Net readiometer via connector 3 (6 pin)
5H - Red
5L - Blue
5L - Jumper to AG
G - Black
 
CR1000 - ARG100 Rain gauge via connector 4 (6 pin)
G - Clear
G - Yellow
P2 - Black

CR1000 - Primary effluent tipping bucket
C6 - Yellow/Green (with black heat shrink)
5V - Yellow/Green (with yellow tape)
  
CR1000 - Secondary effluent tipping bucket
C8 - Yellow/Green (with black heat shrink)
5V - Yellow/Green (with yellow tape)

CR1000 - GS3 VWC sensors
SW12V - White
G - Bare
C5 - Red
SDI-12 address: 1,2,3,4
 
CR1000 - Color - Multiplexer AM16/32B(1)
G - Black - G
G - Yellow - COM G
12V - Red - 12V
C1 - White - CLK
C2 - Blue - RES
VX1 - Green - COM ODD H
1H - Orange - COM ODD L
1L - Grey - COM EVEN H
2H - Purple - COM EVEN L
  
CR1000 - Color - Multiplexer AM16/32B(2)
G - Black - G
G - Yellow - COM G
12V - Red - 12V
C1 - White - CLK
C3 - Blue - RES
VX1 - Green - COM ODD H
2L - Orange - COM ODD L
3H - Grey - COM EVEN H
3L - Purple - COM EVEN L

Wiring of EC5 VWC sensors on multiplexers
ShortID - Variable - Connection - White(pwr) - Bare(G) - Red(data)
#E01 - E5(1) - AM16/32B(1) - 1H - 1G - 1L
#E02 - E5(2) - AM16/32B(1) - 1H - 1G - 2H
... - ... - ... - ... - ... - ...
#E48 - E5(48) - AM16/32B(1) - 31H - 31G - 32L
#E49 - E5(49) - AM16/32B(2) - 1H - 1G - 1L
... - ... - ... - ... - ... - ...
#E80 - E5(80) - AM16/32B(2) - 21H - 21G - 22H
#E81 - E5(81) - AM16/32B(2) - 21H - 21G - 22L

