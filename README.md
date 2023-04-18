# kubecon-chaoshub

This repository contains example chaos workflows using the LitmusChaos hub for injecting chaos into Kubernetes clusters. The workflows are designed to test the resilience and reliability of applications running on Kubernetes by simulating various failure scenarios.

## Chaos Workflows

The following chaos workflows are included in this repository:

### 1. boutique-cart-pod-delete

This workflow injects chaos by deleting a pod in the boutique-cart deployment. It tests the resilience of the boutique-cart application to pod failures.

#### Steps:
1. Install the boutique-cart application.
2. Delete a pod in the boutique-cart deployment using the LitmusChaos pod-delete experiment.
3. Verify the application's behavior during pod deletion.
4. Restore the deleted pod and verify the application's recovery.

### 2. boutique-cart-pod-cpu-hog

This workflow injects chaos by hogging CPU resources in a pod of the boutique-cart deployment. It tests the resilience of the boutique-cart application to high CPU utilization scenarios.

#### Steps:
1. Install the boutique-cart application.
2. Hog CPU resources in a pod of the boutique-cart deployment using the LitmusChaos pod-cpu-hog experiment.
3. Verify the application's behavior during CPU resource hogging.
4. Stop hogging CPU resources and verify the application's recovery.

## Prerequisites

Before running the chaos workflows, ensure that you have the following prerequisites:

- A Kubernetes cluster with LitmusChaos installed.
- The boutique-cart application deployed in the cluster.

## Usage

To run the chaos workflows, follow these steps:

1. Add this repository to the external hub in chaos center
2. Navigate to run workflow and select any one of the workflows (e.g., `kubecon-chaoshub/boutique-cart-pod-delete` or `kubecon-chaoshub/boutique-cart-pod-cpu-hog`).
3. Run the workflow in inject chaos on boutique microservice.
4. Monitor the chaos experiment and observe the behavior of the boutique-cart application during the chaos.

## Contributing

If you would like to contribute to this repository, please follow the standard GitHub fork and pull request workflow. Contributions are welcome and encouraged!

## License

This repository is licensed under the [MIT License](LICENSE).

## References

For more information about LitmusChaos and chaos engineering in Kubernetes, refer to the following resources:

- [LitmusChaos Documentation](https://docs.litmuschaos.io/)
- [LitmusChaos GitHub Repository](https://github.com/litmuschaos/litmus)
- [Chaos Engineering Principles](https://principlesofchaos.org/)
