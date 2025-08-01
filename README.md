# Personalized Graph Federated Learning Based on Unlearning

![](https://img.shields.io/badge/Python-3.9.16-green) ![](https://img.shields.io/badge/PyTorch-2.0.1-blue) ![](https://img.shields.io/badge/PyTorch_Geometric-2.3.0-red)
# Abstract
The demand for personalized services across various fields, particularly in privacy-sensitive domains such as healthcare and finance, has made Personalized Federated Graph Learning (PFGL) increasingly relevant. However, existing federated learning (FL) methods struggle with key challenges, including effective personalization, scalability, and the ability to adapt to dynamic user preferences. In this paper, we propose a novel algorithm, Customized Federated Graph Learning (CFGL), which leverages both structural and behavioral information from users’ graph data to enhance personalization and improve model generalization. CFGL introduces an innovative preference unlearning mechanism, allowing the model to efficiently forget non-preference data while preserving user privacy and maintaining model accuracy. Our method is designed to scale effectively across large datasets, adeptly handling diverse user needs and complex graph structures with minimal computational overhead. Extensive experimental evaluations on real-world datasets demonstrate that CFGL significantly outperforms existing methods in terms of accuracy, personalization, and efficiency. By addressing the limitations of traditional approaches, CFGL provides an effective solution for real-time, user-centered applications, ensuring robust and adaptive performance in rapidly changing environments.

# Algorithm
As depicted in figure, the proposed CFGL framework consists primarily of two key components: Structural Extraction (STE) and Preference Unlearning (PFU). These two components work in tandem to address the challenges of both personalized learning and preference-based model customization in a federated environment.

<img src="/doc/overview.png" width="100%" height="100%">

The STE module identifies the underlying structure of clients' graph data using parameter and behavioral similarities. It preserves privacy by constructing a client structural graph, where nodes represent clients and edges reflect model similarities. This graph is clustered to group clients for personalized learning.

<img src="/doc/ste.png" width="50%" height="50%">

The PFU module enables personalized model refinement by separating each client's data into preference and non-preference subgraphs. Non-preference data is unlearned, and preference data is used to fine-tune the model, ensuring customization without reliance on irrelevant information.

<img src="/doc/pfu.png" width="50%" height="50%">

Together, STE and PFU address structural and personalization challenges in federated learning while ensuring privacy and efficiency.  

