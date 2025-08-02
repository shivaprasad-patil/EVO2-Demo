# EVO2-Demo
Working implementation of a StripedHyena-based neural network architecture designed for DNA sequence modeling.

| Feature               | Notebook Hyena Layers           | Evo2 Hyena Layers (Official)      |
|-----------------------|----------------------------------|------------------------------------|
| **Model Size**        | 128–1024 hidden size (demo)     | 7B–40B parameters                  |
| **Core operation**    | Grouped attention-like convolution | Implicit long convolution (FFT, SSM) |
| **Tokenizer**         | Simple char-level for DNA       | Byte-Level                         |
| **FFT/State-space**   | ❌ Not used                     | ✅ Used for efficiency             |
| **Gating/Modulation** | ❌ Not present                  | ✅ Present in some variants        |
| **CUDA optimization** | ❌ Pure PyTorch                 | ✅ Custom CUDA kernels             |
| **Scalability**       | Small/medium models             | Large models, long sequences       |
| **Intended use**      | Educational, prototyping        | Production, research               |
