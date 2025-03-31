# Full-metal RC-TANK in 1:11 Scale
Project of full-metal RC-TANK in 1:11 scale made from 3mm thick steel sheets  
### Requirements:
1. Dimensions  

| Dimension    |         |
|--------------|---------|
| $Length$     | 70 [cm] |
| $Width_{1}$  | 32 [cm] |
| $Width_{2}$  | 42 [cm] |
| $Height$     | 20 [cm] |
| $Ground\ clearance$ | 5 [cm] |

###### $Width_{1}$ - Width of tank without tracks  
###### $Width_{2}$ - Width of tank with tracks  
2. Maximum speed  of at least $V_{Max}=5\frac{km}{h}$  
3. Input battery voltage $U_{In}=12.5V - 35V$  
4. DC Motors voltage $U_{m}=7.2V$  
### Tracks and sprocket wheels

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/Tank_Tracks.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/Tank_Tracks.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/Tank_Tracks.png">
</picture>

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/Sprocket_Wheel.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/Sprocket_Wheel.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/Sprocket_Wheel.png">
</picture>

### DC Motors selection
<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/Injora540_13T_Parameters.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/Injora540_13T_Parameters.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/Injora540_13T_Parameters.png">
</picture>

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/Injora540_Parameters_Comparison.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/Injora540_Parameters_Comparison.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/Injora540_Parameters_Comparison.png">
</picture>

According to graphs Injora 540 13T has the highest peak power of around 300W but its RPM is too high for usage in a RC Tank. In order to able to move heavy vehicle we need to use a gearbox.

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/DC_Motor_Selection.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/DC_Motor_Selection.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/DC_Motor_Selection.png">
</picture>

### Gearbox selection   
<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/DC_Motor_Gearbox_1_50.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/DC_Motor_Gearbox_1_50.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/DC_Motor_Gearbox_1_50.png">
</picture>

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/DC_Motor_Gearbox_dims_1.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/DC_Motor_Gearbox_dims_1.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/DC_Motor_Gearbox_dims_1.png">
</picture>

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/DC_Motor_Gearbox_dims_2.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/DC_Motor_Gearbox_dims_2.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/DC_Motor_Gearbox_dims_2.png">
</picture>

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="Drivetrain/DC_Motor_Gearbox_Selection.png">
 <source media="(prefers-color-scheme: light)" srcset="Drivetrain/DC_Motor_Gearbox_Selection.png">
 <img alt="YOUR-ALT-TEXT" src="Drivetrain/DC_Motor_Gearbox_Selection.png">
</picture>

Speed of the tank has to be at least $V_{Max}=5\frac{km}{h}$

| Drivetrain parameters    |         |
|--------------|---------|
| $Sprocket wheel diameter$     | D=48 [mm] |
| $RPM$  | n=32500 [rpm] |
| $Gearbox eduction$  | r=1:50 |

We can see that the selected DC motor with 1:50 gearbox gives theoretical 650 rpm.

Using a formula 1) we can calculate maximum theoretical speed of a tank.

1) $V_{Max}=\pi\frac{D*rpm}{60}=1.63\frac{m}{s}=5.88\frac{km}{h} $

