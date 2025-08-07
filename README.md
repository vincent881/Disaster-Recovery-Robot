# Disaster-Recovery-Robot

![Untitled video - Made with Clipchamp (1)](https://github.com/user-attachments/assets/adb5efb1-b2f3-48cd-aa48-24583c4e19de)

## A.	Describe the disaster recovery environment you chose and the two obstacles you have added to the environment.
- The chosen disaster recovery environment is a flooded zone, where a rescue robot is searching and identifying trapped humans. In the simulation, the floor mimics a water surface, and the robot must navigate in an enclosed flooded area.
- In the scenario, two large cuboids are representing floating debris.
- The long cuboids represent collapsed walls, trapping the human inside.
- These simulate real obstructions in a flood scenario, where fallen structures and debris block line of sight and movement.
## B.	Explain how the robot will improve disaster recovery in the environment from part A after you have added the two obstacles from A.
- The robot improves disaster recovery by: autonomously navigating the flooded environment, using proximity sensors to avoid debris and barriers, using a dedicated sensor to identify humans, and sending a status message when a human is located. In a real scenario, this robot could relay coordinates or trigger alerts for emergency teams, increasing response times and lives saved.
## C.	Justify the modifications you made to CoppeliaSim’s robot architecture, including two sensors you chose to add, and explain how these sensors will aid the disaster recovery effort.
- The original BubbleRob was modified with two proximity sensors. The first added, sensingNose[1], detects only the target human using proximity detection and object name matching. The second sensor, sensingNose, is used for obstacle detection and triggering reverse motion if anything is detected ahead of the robot.
- These sensors help the robot avoid obstacles, navigate safely, locate humans, and identify humans precisely among the clutter.
## D.	Describe how the robot maintains an internal representation of the environment.
- The robot uses proximity-based awareness with real time sensor data which drives reactive movement (forwards and backwards).
- The robot uses distance measurements that are stored in a graph to visualize clearances over time. This is useful for analysis and debugging.
- These show that the robot maintains an internal representation. 
## E.	Explain how the robot implements the following four concepts to achieve its goal:
- Reasoning: The robot switches between forward and reverse modes based on whether an obstacle is detected.
- Knowledge Representation: Uses sensor values and object identifiers to represent knowledge of the world.
- Uncertainty: Sensor readings may be imperfect, so the robot uses continuous feedback to handle this uncertainty.
- Intelligence: The robot exhibits autonomous behavior. It navigates, senses, decides when to change direction, and identifies victims without human intervention.
## F.	Explain how the prototype could be further improved, including how reinforced learning and advanced search algorithms can improve the prototype’s performance and learning.
- Reinforced learning could be used to train the robot to optimize its path, learning to reach humans faster and avoiding collisions.
- Advanced search algorithms could provide more intelligent navigation toward known human coordinates, improving efficiency in larger disaster zones.
- Simultaneous localization and mapping could let the robot build a map of the environment in real time.
- These upgrades would enable dynamic and intelligent exploration decision making, and adaptation to unpredictable flood environments.

