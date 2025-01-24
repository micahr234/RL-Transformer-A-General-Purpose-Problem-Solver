# RL + Transformer = A General-Purpose Problem Solver

This repository contains the code and experiments for our paper:

**RL + Transformer = A General-Purpose Problem Solver**

In this work, we demonstrate that fine-tuning a pre-trained transformer with reinforcement learning enables it to function as a general-purpose problem solver. The model develops the ability to solve problems it has never encountered before—an emergent ability called **In-Context Reinforcement Learning (ICRL)**.

## Overview

Our experiments show that an RL-trained transformer:

- Excels in solving unseen in-distribution environments with remarkable sample efficiency.
- Shows strong performance in out-of-distribution environments.
- Exhibits robustness to the quality of its training data.
- Seamlessly stitches together behaviors from its context.
- Adapts to non-stationary environments.

These behaviors demonstrate that an RL-trained transformer can iteratively improve upon its own solutions, making it an excellent general-purpose problem solver.

## Repository Structure

- `code/`: Contains the implementation of the ICRL training and evaluation procedures.
- `data/`: Scripts for data generation and preprocessing.
- `models/`: Code related to model architecture and fine-tuning.
- `README.md`: Project overview and instructions.
- `LICENSE`: License information.

## Getting Started

### Prerequisites

- Python 3.8 or higher
- PyTorch
- Hugging Face Transformers
- Gymnasium (for environment simulations)
- Additional dependencies listed in `requirements.txt`

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your_username/icrl-transformer.git
   cd icrl-transformer
   ```

2. **Create a virtual environment and activate it:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```

### Running Experiments

**Training the Model:**

Fine-tune the pre-trained transformer with:

```bash
python code/train_icrl.py --config configs/train_config.yaml
```

**Evaluation:**

Evaluate the trained model on new environments:

```bash
python code/evaluate_icrl.py --config configs/eval_config.yaml
```

**Plotting Results:**

Generate plots from the results:

```bash
python experiments/plot_results.py
```

## Results

Our experiments demonstrate the capabilities of the ICRL-trained transformer across various tasks, including:

- Solving unseen in-distribution and out-of-distribution examples.
- In-context behavior stitching to combine learned skills.
- Robustness to low-quality training data.
- Adaptation to non-stationary environments.

For detailed results and discussion, please refer to the `results/` directory and the paper.

## Citation

If you find this work useful, please cite our paper:

```bibtex
@article{rentschler2025icrl,
  title={RL + Transformer = A General-Purpose Problem Solver},
  author={Rentschler, Micah and Roberts, Jesse},
  journal={Proceedings of the International Joint Conference on Artificial Intelligence (IJCAI)},
  year={2025}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## Acknowledgments

We would like to thank the open-source community and the developers of LLaMA and related tools that made this research possible.


## Contact

For any questions or issues, please open an issue on this repository or contact us at:

- Micah Rentschler: [mrentschler@tntech.edu](mailto:mrentschler@tntech.edu)
- Jesse Roberts: [jroberts@tntech.edu](mailto:jroberts@tntech.edu)

## Dataset can be found at

https://huggingface.co/datasets/micahr234/FrozenLakeNotSlipperyPrepared20eto40ecombineto4096
https://huggingface.co/datasets/micahr234/FrozenLakeNotSlipperyPrepared20eto40ecombineto4096low
https://huggingface.co/datasets/micahr234/FrozenLakeNotSlipperyPrepared20eto40ecombineto4096hi

