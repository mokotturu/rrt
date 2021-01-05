# RRT
 
Rapidly-exploring Random Trees (RRT) is an algorithm designed to efficiently search spaces by randomly building a space-filling tree.  The tree is constructed incrementally from samples drawn randomly from the search space and is inherently biased to grow towards large unsearched areas of the problem. RRTs were developed by Steven M. LaValle and James J. Kuffner Jr. They easily handle problems with obstacles and differential constraints (nonholonomic and kinodynamic) and have been widely used in autonomous robotic motion planning.

An RRT grows a tree rooted at the starting configuration by using random samples from the search space. As each sample is drawn, a connection is attempted between it and the nearest state in the tree. If the connection is feasible (passes entirely through free space and obeys any constraints), this results in the addition of the new state to the tree.

The length of the connection between the tree and a new state is frequently limited by a growth factor. If the random sample is further from its nearest state in the tree than this limit allows, a new state at the maximum distance from the tree along the line to the random sample is used instead of the random sample itself. The random samples can then be viewed as controlling the direction of the tree growth while the growth factor determines its rate. This maintains the space-filling bias of the RRT while limiting the size of the incremental growth.

This project starts with a plane and three fixed obstacles (whose coordinates can be changed through code). Two points - start and goal - are chosen randomly. The blue circle is the start position and the green circle is the goal. A tree is built starting from the start position until one of the nodes finds the goal. Once the goal is found, a path is drawn from the start to the goal position in red color. The total number of nodes added to the tree is updated constantly and is shown at the top.

Link: https://mokotturu.github.io/rrt/
