# Pytorch_DeepLearning

Learning Pytorch

# Pytorch Installation for CPU

    conda install pytorch torchvision torchaudio cpuonly -c pytorch

# AutoGrad

    Why do we require AutoGrad?

    When we do BackPropagation we need to calculate gradient of loss function wrt weights
    If we do gradient calculation with hands it will take time and it wont be dynamic as then we would have to write each derivative manually
    To resolve this issue Pytorch has a capability to calculate derivative of functions automatically which is known as AutoGrad.

    A simplified model of a PyTorch Tensor is an objecct containing the following properties:

        1. Data - A self reference
        2. required_grad - whether or not this tensor is/should be connected to the computational Graph
        3. grad - if require_grad is true, this prop will be a sub-tensor that collects the gradients against this tensor accumulated during BackPropagation
        4. grad_fn - This is a reference to the most recent operation which generated this tensor.Pytorch performs automatic differentiation by looking through the grad_fn list.
        5. is_leaf - whether or not this is a leaf node.
