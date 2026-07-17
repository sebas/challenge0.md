# challenges.md


1. **Why is the first route discovered not necessarily the shortest route?**
   The first route found may be longer than another route discovered later. Dijkstra’s algorithm compares all tentative distances before deciding which route is shortest.

2. **Why can a finalized node no longer receive a shorter distance?**
   A node is finalized only when it has the smallest tentative distance. Since all road distances are nonnegative, no later route can make its distance smaller.

3. **What is the difference between a tentative distance and a finalized distance?**
   A tentative distance is the best distance found so far and can still change. A finalized distance is confirmed as the shortest possible distance and will not change.

4. **How did the previous-node column help you reconstruct the route?**
   The previous-node column shows which node was used to reach each node with the shortest distance. Starting at the destination, we follow the previous nodes backward until reaching the starting node.

5. **What would happen if one road had a negative distance?**
   Dijkstra’s algorithm could produce the wrong answer because a finalized node might later receive a shorter distance. A different algorithm, such as Bellman–Ford, should be used for negative distances.

