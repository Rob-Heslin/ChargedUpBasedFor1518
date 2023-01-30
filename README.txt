To bring up this swerve drive follow the followingg steps.
1. Confirm robot is off the ground, After Loading the code on the robot, keep the robot disabled.
2.Run the command DriveAdjustModulesManually while disabled.
3. Check the following:
-rotate the modules counterclockwise, both the AbsAngle and RelEnc should increase in value
-point the all wheels forward. move drive wheels as if driving forward, expect positive distancce changes and veleocity
4. If checks ok, run DriveResetAllModulePositionsToZero, wait for 10 seconds
5. Enable robot, run Drive Module 0,1,2 or 3, move motors must have output for rotation to happen, Dpad gives angles to rotate to
-Check if rotation PID is tuned, tune as needed, constants in Constants 
6. Now run DriveRobotCentric, this can be enabled as the default command in RobotContainer line 89, drive to test that robot drive forward, backward left right, etc.
7. With Robot disabled, check that gyro/imu is working, rotate robot check to see that Gyro values on Dashboard change positive with counter clockwise rotation
8. Now try DriveFieldRelative, this can be enabled on line 90 of RobotContainer, confirm field relative drive works as expected
9. Figure out the move PIDF values you need, this will let you move from Duty cycle to Velocity PID on drive modules 
10. Test DriveTurnToAngle, this will give a base line for rotational PID
11. Adjust the counter rotation PID for running DriveFieldCentricAdvanced
