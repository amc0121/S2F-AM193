# S2F-AM193
S2F-AM193 tiltwing eVTOL vehicle data, including mass properties and linear model data

Vehicle Properties:
Mass = 8.163 (kg)
Weight = 80.079 (N)
Main Propellers (tilting) = APC 16x10E(P)
Tail Propeller = APC 10x45MR(P)
Ixx = 1.185 (kg-m2)
Iyy = 0.735 (kg-m2)
Izz = 2.085 (kg-m2)

Information to interpret the trim table results:

Case: trim case number (used to specify a specific trim condition)

KEAS: freestream velocity for trim (kts)
FPA: flightpath angle (deg) specified for trim (0 = no climb rate)
AOA: angle of attack (deg) to achieve trim
BETA: sideslip angle (deg) to achieve trim
ULAT: normalized lateral control group input (-1,+1) before the control mixer/allocator, representing "roll" control authority from -100% to +100%
ULON: normalized longitudinal control group input (-1,+1) before the control mixer/allocator, representing "pitch" control authority from -100% to +100%
UDIR: normalized directional control group input (-1,+1) before the control mixer/allocator, representing "yaw" control authority from -100% to +100%
NAC: angle of the propeller/motor nacelles (not necessarily the wing if the motors are mounted with incidence) | equivalent to TAI: thrust axis inclination angle (+90 is vertical)
FLAP: flap setting (deg)
MP_RPM: Main-prop (propellers that help with cruise flight) RPM at trim
LP_RPM: Lift-prop (or vertical lift propellers) RPM at trim
TAI: Thrust-axis inclination angle at trim (deg, commonly “Thrust Axis Inclination”)
TW_MP: Main-prop thrust-to-weight ratio (T/W)
X: 1 x 12 state vector (u;v;w;p;q;r;phi;theta;psi;x;y;z) - SI units
U: 1 x n control effectors vector (u1;u2;...;un) - units in RPM or degrees
Xi: average uniform inflow velocity for each propeller (m/s)
Skew: quasi-steady wake skew angle for each propeller (deg)
r_cg: center of gravity location at trim w.r.t. the vehicle reference point (m) | vehicle reference point is RP = (-17.762,0.000,-1.025) as measured from the vehicle nose in the body-fixed coordinate system
Q_Nm: motor torque at trim (Nm)
P_W: individual motor/propeller power demand at trim (W)
P_tot: total propulsor power demand at trim (W)
LinModel: struct containing linearized model information at each trim condition (also available in the A Matrix, B Matrix, and Eigenvalue folders)
