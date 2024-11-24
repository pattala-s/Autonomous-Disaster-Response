# Autonomous-Disaster-Response
In this project, you will design and implement a complete autonomous system to perform recon- naissance in a simulated disaster environment. Specifically, when introduced into a closed but initially unknown environment, your system should do the following:

1. Generate a complete map of the environment
2. Locate any victims present in the environment
   For the purposes of this exercise, we will represent the environment using an occupancy grid
map, and use AprilTags as stand-ins for simulated victims. Therefore, the specific outputs of
your system corresponding to points (1) and (2) above should be:
1. A complete occupancy grid map of the environment.
2. A list of AprilTags discovered in the environment. Each element of this list must specify:
• The ID (number) of the detected tag
• The pose of the tag, expressed with respect to the map frame.
Rules of the game
You may construct your system using any off-the-shelf components that you like. For example,
you may want to make use of the Cartographer package that to build occupancy grid maps, the
move base package from the ROS navigation stack in order to generate and follow motion plans
to move the robot around the environment, and/or a (basic) frontier exploration package such
as explore lite.
However, you should consider that a baseline system constructed solely from off-the-shelf
components may not perform very well on the target task. For example:
• While a basic frontier-based exploration planner like explore lite can ensure a complete
map, it does not address the goal of searching for “victims” (AprilTags). You might consider
either modifying explore lite, or implementing your own planner, in order to improve
your system’s ability to find all of the tags present in an environment.
• The (estimated) pose associated with an AprilTag detection can be rather noisy, especially
when the tag is viewed from a distance. You might want to think about possible approaches
for ensuring that the pose of each detected tag is estimated accurately in the final map.
In addition to ROS packages, when implementing your own system you may find the OpenCV
library (especially the image processing module) useful for operating on occupancy grid maps,
and/or the GTSAM library useful for performing parameter estimation, should your approach
require it.






