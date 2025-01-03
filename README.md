# MNIFS
Siyu Yang, **Zhong Yuan***, Chuan Luo, Hongmei Chen, and Dezhong Peng, [Fuzzy multi-neighborhood entropy-based interactive feature selection for unsupervised outlier detection](Paper/2025-MNIFS.pdf), Applied Soft Computing, 2025, vol. 169, no. 112572. DOI: [10.1016/j.asoc.2024.112572](https://doi.org/10.1016/j.asoc.2024.112572).

## Abstract
Unsupervised feature selection is one of the important techniques for unsupervised knowledge discovery, which aims to reduce the dimensionality of conditional feature sets as much as possible to improve the efficiency and accuracy of the algorithm. However, existing methods have the following two challenges: 1) They are mainly applicable to select numerical or nominal features and cannot effectively select heterogeneous features; 2) The relevance and redundancy are primarily considered to construct feature evaluation indexes, ignoring the interaction information of heterogeneous features. To solve the challenges mentioned above, this paper proposes an unsupervised heterogeneous feature selection method based on fuzzy multi-neighborhood entropy, which also considers the multi-correlation of features to select heterogeneous features. First, the fuzzy multi-neighborhood granule is constructed by considering the distribution characteristics of the data. Then, the concept of fuzzy entropy is introduced to define the fuzzy multi-neighborhood entropy and its associated uncertainty measures, and the relationship between them is discussed. Next, the relevance, redundancy, and interactivity among attributes are defined, and the idea of maximum relevance-minimum redundancy-maximum interactivity is used to construct the evaluation indexes of heterogeneous features. Finally, experiments are conducted on several publicly unbalanced datasets, and the results are in comparison with existing algorithms. The experimental results show that the proposed algorithm can select fewer heterogeneous features to improve the efficiency of outlier detection tasks.
## Framework
![image](Paper/MNIFS-Framework.png)
## Usage
You can run MNIFS.py:
```
if __name__ == "__main__":
     # Import data
    Example = loadmat('Example.mat')
    trandata = np.array(Example['Example'])

    # Normalization process for numerical data
    min_max_scaler = preprocessing.MinMaxScaler()
    trandata[:, 0:2] = min_max_scaler.fit_transform(trandata[:, 0:2])

    # Set the threshold lammda
    lammda = 1

    feature_seq, sig = MNIFS(trandata, lammda)
    print(feature_seq)
```
You can get outputs as follows:
```
feature_seq = [0, 1, 3, 2]
```

## Citation
If you find MNIFS useful in your research, please consider citing:
```
@article{yang2025fuzzy,
  title={Fuzzy multi-neighborhood entropy-based interactive feature selection for unsupervised outlier detection},
  author={Yang, Siyu and Yuan, Zhong and Luo, Chuan and Chen, Hongmei and Peng, Dezhong},
  journal={Applied Soft Computing},
  pages={112572},
  year={2025},
  publisher={Elsevier}
}
```
## Contact
If you have any questions, please contact yuanzhong@scu.edu.cn.
