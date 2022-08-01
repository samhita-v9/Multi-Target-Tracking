# Multi-Target-Tracking
A GPU Accelerated Dual-Ascent Algorithm for the Multidimensional Assignment Problem in a Multitarget Tracking Application


The full paper is available at https://ieeexplore.ieee.org/document/9808104. 

Abstract:

We develop a Graphics Processing Unit (GPU) accelerated algorithm for the NP-Hard Multi-dimensional Assignment Problem (MAP), suitable for target tracking applications. First, the original MAP formulation with a quadratic objective function is reformulated using a creative linearization technique. This formulation lends itself well to Lagrangian Relaxation, which decomposes into pairwise Linear Assignment Problems (LAPs). These LAPs are solved in parallel and are each solved using a recent GPU-accelerated approach. Next, we propose a dual-ascent scheme for the Lagrange multiplier updates. The advantage of this scheme is that it results in monotonically increasing lower bounds and converges in a fraction of the iterations typically needed for a subgradient method. The dual-ascent technique is also parallelized for the GPU. Finally, we develop a creative gap closure scheme with $M$ -best LAP solutions for each dimension and find the shortest path in the resulting staged graph. The algorithm is applied to the Multi-Target Tracking problem and tested on datasets for maneuverable targets. Scaling studies are also performed, and note that the processing time goes down approximately linearly in the number of GPU devices. The algorithm can efficiently solve up to a problem size of 400 targets in 400 time-frames, which corresponds to 25 billion variables, with high accuracy. 


Note to Practitioners:

The Multi-Target Tracking problem (MTT) has been a longstanding problem with various variants and solution algorithms. Still, the problem remains challenging, especially when dealing with a large number of targets for many time frames, when solution speed and optimality are concerns. Many problems including, entity resolution, weapon target assignment, resource allocation, and data association can be formulated as MAP. Our overall algorithm, implemented with GPU acceleration enables addressing large-dimensioned MAPs, e.g., number of observed targets for a long horizon, for around 25 billion variables. As per our knowledge, no algorithm could tackle this large-scale data either for MAP or MTT.

