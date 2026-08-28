## Unsupervised-Image-Segmentation-Using-Quantum-Annealing
Keywords : Quantum computing, Quantum annealing, Quadratic Unconstrained Binary Optimization, Image segmentation, Graph simplification <br>
<div align="justify">
  Image Segmentation is a primary step in image processing, identifying independent regions in an image. Graph-based techniques leverage the structural similarity between images and graphs; pixels correspond to nodes and pixel similarities to edges. In this framework, binary image segmentation can be formulated as a weighted graph-cut problem that is generally NP-hard and beyond the efficient reach of classical computing. However, quantum annealing can directly solve the problem by leveraging the mathematical equivalence between Quadratic Unconstrained Binary Optimization (QUBO) and the Ising model. Consequently, finding the system’s ground state yields optimal segmentation. In this work, we present the following contributions to address limitations of previous studies. First, we rectify their QUBO formulations and thereby demonstrate authentic image segmentation using quantum annealing. Second, we introduce a contrast-based node sampling method that considerably reduces the required number of qubits and their connections. Since contrast is key for boundary detection, we define node importance as proportional to contrast with neighboring nodes. For noisy images, a node’s importance is updated by aggregating the importance scores of its neighbors. After random-sampling less important nodes and adding them to the subgraph of highly important nodes, we restore connectivity between nodes along the grid axes and thereby enable graph-cut to capture broader context. All our subroutines run in linear time with the number of nodes, ensuring scalability. We evaluate our method with the D-Wave Advantage quantum annealer on both small- and large-scale datasets: the Fashion-MNIST dataset (repurposed for foreground-background segmentation by thresholding) and the DeepGlobe 2018 road extraction dataset. While an existing baseline yields trivial solutions across both datasets, our corrected QUBO formulation achieves reliable segmentation on the small dataset with high scores across all evaluation metrics. Although our formulation initially exhibits limitations on satellite imagery, our node sampling method resolves this issue with minimal overhead—accounting for 9.6% of the annealing time—and boosts all the metrics by +30.8% to +76.3%. At the same time, our method achieves substantial quantum resource savings, reducing qubits and their connections by 95.4% and 95.4%, respectively, and accordingly reducing annealing time by 93.6%. Our quantum-classical hybrid approach demonstrates how strategic classical computing guides quantum annealers towards optimal solutions, reduce qubit demand to fit current hardware limits, and thereby unlock practical image segmentation on commercial quantum hardware. <br>

<p align='center'><img src="img/flowchart.png" width="600"/></p>
    
### Datasets
</div>
<div align="justify">
  TEST
  <ul>
    <li>Fashion MNIST, repurposed for object-background segregation</li>
  </ul>
  Binary segmentation
  <ol>
    <li><a href='https://www.kaggle.com/datasets/balraj98/deepglobe-road-extraction-dataset'>DeepGlobe 2018 road extraction</a></li>
    <li><a href='https://github.com/iai-postech/OpenSource/tree/main/weakly_supervised_microstructure_segmentation'>Spheroidite particles</a></li>
    <li>...</li>
  </ol>
  Multi-class segmentation
  <ol>
    <li></li>
  </ol>
</div><br>

### Benchmarks
</div>
<div align="justify">
  <ol>
    <li><a href='https://github.com/supreethmv/Q-Seg'>Q-Seg: Quantum Annealing-Based Unsupervised Image Segmentation</a></li>
    <li><a href='https://pytorch.org/hub/pytorch_vision_deeplabv3_resnet101/'>Deeplabv3</a></li>
    <li><a href='https://github.com/facebookresearch/segment-anything'>Segmentation Anything Model (SAM)</a></li>
    <li>...</li>
  </ol>
</div>
