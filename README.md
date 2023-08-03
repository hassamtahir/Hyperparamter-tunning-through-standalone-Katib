# Hyperparamter tunning through standalone Katib
Katib (also known as "Kubeflow Katib") is an open-source hyperparameter tuning system developed by the Kubeflow community. It is designed to automate the process of hyperparameter optimization for machine learning models running on Kubernetes clusters. Hyperparameter tuning is a critical step in the machine learning workflow, as it involves finding the best combination of hyperparameters that optimize the model's performance and generalization.

Here are some key features and concepts of Katib:

Hyperparameter Tuning: Katib allows users to define the hyperparameters and their search spaces for a machine learning model. It supports various search algorithms, including random search, grid search, and Bayesian optimization, among others. Katib automatically explores different combinations of hyperparameters to find the configuration that yields the best performance.

Kubernetes Integration: As part of the Kubeflow ecosystem, Katib leverages Kubernetes for orchestrating the hyperparameter tuning jobs. It takes advantage of Kubernetes' scalability and resource management capabilities, allowing users to efficiently conduct distributed hyperparameter tuning experiments.

Early Stopping: Katib supports early stopping strategies to terminate underperforming experiments early, saving time and resources.

Metric Collection: During hyperparameter tuning, Katib collects and logs metrics from each training run. These metrics are used to evaluate the performance of different hyperparameter configurations.

Integration with Other Kubeflow Components: Katib can be integrated with other Kubeflow components like TensorFlow, PyTorch, and other machine learning frameworks, enabling seamless experimentation and training on Kubernetes.

# Experimental Steps
Step#1:
Cross check katib installation and its components:
![1](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/5da63ed1-d4c3-4175-902e-d91cbe0beb0e)

![2](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/022cc1db-7903-42d4-b114-53af3bbe6362)

Step#2: Define hierarchy of experimentation:
<img width="343" alt="3" src="https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/22015721-6504-4138-8a97-7aa830f5f9c1">
![4](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/490c5f4c-ce2a-40d6-9044-50880777bc9c)

Step#3: Check python code to be executed:
![5](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/0920ba95-e655-42bf-80dd-f5bd461b1caf)

![6](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/bbc3c2e3-d1ef-46b7-b23e-bf4d67ed29cf)

Step#4: Defining hyperparameter Yaml File:
![7](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/ee482dbd-13b3-4a5e-99ee-b2d1b7130b63)

Step#5: Command to apply yaml file: 
kubectl appy –f <path to yaml file>
![8](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/26624cc5-6dd9-4dcc-81eb-1194b1fbd2d9)

Step#6: Run & Check experiment status
![9](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/51780d95-1735-494b-9cc3-8c453c3b62be)

![10](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/d728733d-f14d-4bfb-a1b2-bed09592584d)

Step#7: Acces container inside pod to observe logs and epoch acurracy of machine learning model:
--> Check logs of metric collector container
![11](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/a0e293a2-8710-4887-bb64-2dccf979e5e3)

![12](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/4e0c6148-24c1-4192-b358-ebf2eb0db162)

Step#8: Best trial and result collection according to user:

![13](https://github.com/hassamtahir/Hyperparamter-tunning-through-standalone-Katib/assets/58023371/44222c48-39f2-4c9d-870f-b80aced22acd)




