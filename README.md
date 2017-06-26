# Exploring difference in $\mathrm{KL}(P \Vert Q)$ vs $\mathrm{KL}(Q \Vert P)$ 

In this notebook, we investigate different diverngence loss metrics in a simple optimization problem.

## Key Learnings

- P || Q and Q || P looked quite similar qualitatively when the inter-modal separation in the posterior is small. 
    
    ![small_inter-modal_separation](./Comparing%20KL%20P%20Q%20vs%20KL%20Q%20P%20with%20small%20separation.png)
    
    The textbook behavior only ariese when this separation is large, in which case the Gaussian end up optimize towards one of the modes in a local minima.
    
    ![large inter-modal separation](./Comparing%20KL%20P%20Q%20vs%20KL%20Q%20P%20with%20large%20separation.png)
    
- $\mathrm{KL}(P \Vert Q)$ gives an approximation that emcompasses the entire distribution $P$ because $\mathrm{KL}(P\Vert Q) blows up where $Q(x)$ is zero.

- $\mathrm{KL}(Q \Vert P)$ gives an approximation that fits to one of the modes in a local minima.

### Reference:
- Bishop, *Pattern Recorgnition and Machine Learning, Chapter 10*.