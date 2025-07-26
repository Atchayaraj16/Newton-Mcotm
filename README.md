Newton-Enhanced MCOTM: Mobility-Aware Computation Offloading and Task Migration

  This repository provides a Python implementation of the **Newton-enhanced MCOTM** (Mobility-aware Computation Offloading and Task Migration) algorithm for Wireless-Powered Mobile-Edge Computing in **Industrial IoT (IIoT)** environments. 
  It enhances the original MCOTM by improving the trajectory prediction module with **Newton Forward Interpolation**, offering better computational efficiency and numerical stability.


About This Project:

Newton-MCOTM builds upon the original DDPG-based MCOTM framework and improves adaptability in dynamic mobile-edge environments by:

- Replacing Lagrange interpolation with **Newton Forward Interpolation** for accurate and stable mobility prediction  
- Forecasting edge resource availability using **LSTM networks**  
- Leveraging **Deep Deterministic Policy Gradient (DDPG)** to make intelligent decisions on:

- Task offloading  
- Task migration  
- Resource allocation  


Dataset:

This project utilizes real-world data from the **Alibaba Cluster Trace Program**:

- Dataset: Alibaba Cluster Trace v2018  
- Usage: Extracted CPU, memory, and GPU usage metrics are preprocessed and stored in `updated_pod_list.csv`  
- Purpose: Enables realistic modeling of fluctuating edge server resources for training the LSTM prediction model  
- License: Refer to [Alibaba Cluster Trace Repository](https://github.com/alibaba/clusterdata) for terms of use  


 Requirements:

Install required packages:

pip install tensorflow numpy scipy pandas matplotlib scikit-learn

How to Run:

python newton_mcotm.py

Features:

- Newton Interpolation for stable and efficient trajectory prediction
- LSTM-based forecasting for dynamic edge resource modeling
- DDPG agent for adaptive offloading and migration decisions
- Cost-aware migration strategy to balance latency and energy usage
- Fully configurable simulation environment tailored to IIoT constraints

Improvement:


Metric      	          Lagrange-MCOTM	       Newton-MCOTM	       Improvement

Turnaround Time	         142 ms	             131 ms	               **↓ 7.76%**

 
Energy Usage	            0.81 J	              0.75 J	             **↓ 6.96%**


Migration Rate	          50.2%	               47.9%	              **↓ 4.55%**

- Reduces turnaround time by 7–8%
- Lowers energy consumption by ~7%
- Stabilizes migration frequency through predictive control

Reference Paper:
    Predictive Resource Allocation for Mobility-Aware Task Offloading and Migration in Edge Environments"
    Atchaya R, Sakthikanika V, Rakavi Dharshini K, Kannan K, Ezhilarasie R
    School of Computing, SASTRA Deemed University, Thanjavur, India
     Submitted 2025 | Presented at https://icscds.com/|D: ICSCDS466, Aug 8, 2025.
       




