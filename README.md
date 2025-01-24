# RL + Transformer = A General-Purpose Problem Solver

This repository contains the code and experiments for our paper:

**RL + Transformer = A General-Purpose Problem Solver**

In this work, we demonstrate that fine-tuning a pre-trained transformer with reinforcement learning enables it to function as a general-purpose problem solver. The model develops the ability to solve problems it has never encountered before—an emergent ability called **In-Context Reinforcement Learning (ICRL)**.

<img src="https://github.com/user-attachments/assets/1149bcde-7c2f-4023-90e3-3b5fb5e2cb55" width="200"/>
<img src="https://github.com/user-attachments/assets/5266fe98-74ac-4ca1-98e1-5437f5ac0861" width="200"/>
<img src="https://github.com/user-attachments/assets/3359f7ab-34de-4755-b38f-e292cd5edc24" width="200"/>

In the plots above ICRL-trained Llama 3.1 learns to solve an unseen Frozen
Lake environment. The trajectories in early, mid, and late
interactions show solution refinement. Mistakes in early inference
(e.g., falling into holes) disappear with experience in late inference.

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
- `README.md`: Project overview and instructions.
- `LICENSE`: License information.


## Getting Started


### Prerequisites

- Python 3.8 or higher
- PyTorch
- Hugging Face Transformers
- Gymnasium (for environment simulations)


### Running Experiments


**Training the Model:**

Fine-tune the pre-trained transformer with:

Train.ipynb *make sure to add you huggingface username where appropriate*


**Evaluation:**

Evaluate the trained model on new environments:

Eval.ipynb *make sure to add you huggingface username where appropriate*


## License

This project is licensed under the GNU V3 License - see the [LICENSE](LICENSE) file for details.


## Acknowledgments

We would like to thank the open-source community and the developers of LLaMA and related tools that made this research possible.


## Contact

For any questions or issues, please open an issue on this repository or contact us at:

- Micah Rentschler: [mrentschler@tntech.edu](mailto:mrentschler@tntech.edu)
- Jesse Roberts: [jroberts@tntech.edu](mailto:jroberts@tntech.edu)


