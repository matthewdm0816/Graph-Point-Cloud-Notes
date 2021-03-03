### A Note Of Alchemist

###### Kamazi Michiru

| Parameter                                                    | Test/Train Acc      | Notes                                                   |
| ------------------------------------------------------------ | ------------------- | ------------------------------------------------------- |
| DenseGCN+3%Noise+Smooth Label+Weighted Instace+10c Rotation+10% Rescale+10 Ensemble+32 Batch Size+StepAnnealing 0.65@20e | 99+/87.5@<500epoch  |                                                         |
| DenseGCN+3%Noise+Smooth Label+Weighted Instace+10c Rotation+10% Rescale+20 Ensemble+4*32Distributed Training(BN not fixed)+StepAnnealing 0.65@20e | 97.8/85.5@970epoch  | Ensemble10变为20没有显著改进                            |
| DenseGCN+3%Noise+Smooth Label+Weighted Instace+10c Rotation+10% Rescale+5 Ensemble+4*32Distributed Training(BN not fixed)+Cosine Annealing 200e |                     | BN may need to be fixed to SBN                          |
| DenseGCN+3%Noise+Smooth Label0.2+Weighted Instace+10c Rotation+10% Rescale+Random Flip+5 Ensemble+4*32Distributed Training(BN not fixed)+Cosine Annealing 150e | 93.0/85.9@1000epoch | Seems converges quicker at early runs: ? Low confidence |
| DenseGCN+3%Noise+Smooth Label0.1+Weighted Instace+10c Rotation+10% Rescale+Random Flip+5 Ensemble on (0.75-1.25@5)Rescale+4*32Distributed Training(SBN)+Cosine Annealing 200e |                     |                                                         |

