# 598_final
System: 
- 250 mm size quadrotor
- Raspberry Pi 3
- Raspberry Pi camera
- Naze32 FC

Logic:
1. Arm quadrotor
2. Tune roll, pitch, yaw, throttle through the keyboard
3. Initiate tracking loop
4. Read frame in through camera
5. Locate object/face in frame
6. Calculate error of object location and size (desired is in the center of the frame with specified radius)
7. Compute PD control from the error for roll, pitch, throttle
8. Return to Step 4
If tracking is lost for 100 consecutive loops, landing procedure begins
