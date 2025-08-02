# EVO2-Demo
This notebook provides a **complete, working implementation** of a StripedHyena-based neural network architecture specifically designed for DNA sequence modeling. It demonstrates the entire pipeline from model architecture design to successful training with loss curves. This notebook is for 📖 **Educational demonstrations** of the architecture of EVO2.

### 🔬 **Core Functionality**

1. **🧬 DNA Sequence Processing**
   - Custom `CharLevelTokenizer` for genomic data with special tokens (`<PAD>`, `<UNK>`, `<START>`, `<END>`)
   - Handles variable-length DNA sequences with proper padding and tokenization
   - Support for standard nucleotides (A, C, G, T) and ambiguous bases (N, R, Y, etc.)

2. **🏗️ StripedHyena Architecture Implementation**
   - **Multi-scale Convolution Layers**: Short, medium, and long-range dependency modeling
   - **Hybrid Architecture**: Combines convolutional layers with multi-head attention
   - **Optimized for DNA**: Hierarchical pattern recognition from local motifs to long-range interactions

3. **⚡ Advanced Neural Network Components**
   - `RMSNorm`: Root Mean Square normalization for stable training
   - `RotaryEmbedding`: Position-aware embeddings for sequence understanding
   - `MultiHeadAttention`: Self-attention with rotary position encoding
   - `FeedForward`: Efficient feed-forward networks with SiLU activation

### 🚀 **Key Achievements**

#### ✅ **Complete Training Infrastructure**
- `StripedHyenaTrainer` class with comprehensive training loop
- Automatic loss tracking and visualization
- Model checkpointing and validation
- Real-time training progress monitoring

#### ✅ **Successful Training Demonstration**
- Working model that trains on DNA sequence data
- Loss curves showing actual learning progress
- No tensor dimension errors or training failures
- Proper convergence behavior

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
