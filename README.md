<p align="center">
  <img src='logo.png' width=800>
</p>

# [Submitted to ICLR2025] <br> Two Heads Are Better Than One: A Multi-Agent System Has the Potential to Improve Scientific Idea Generation.

## 👀 Introduction

This repository contains the code for our paper `Two Heads Are Better Than One: A Multi-Agent System Has the Potential to Improve Scientific Idea Generation`. 

- To the best of our knowledge, we propose the first multi-agent system for conducting scientific collaborations in an end-to-end pipeline from team organization to novel scientific idea generation. Furthermore, the real data is utilized for role-play and the objective evaluation of final outputs.

- We conduct extensive evaluations to investigate VirSci in terms of the team settings and the novelty of generated scientific ideas. The results demonstrate that multi-agent collaboration can improve the quality of the outcomes, surpassing the SOTA single-agent method.

- The simulation results align with the important findings in Science of Science, such as fresh teams tend to create more innovative research, showcasing the potential of VirSci as a powerful tool for future research in this field.

Our project website is [Website](https://renqichen.github.io/Social_Science/).

## Updates 
📆 [**2024-10**]
1. We propose the VirSci, a multi-agent system has the potential to improve scientific idea generation.
2. Watch demo video for our project at <a href="https://www.youtube.com/watch?v=oMSEAeGfTIk" target="_blank">YouTube</a>.
3. Full paper with Appendix is available on <a href="https://arxiv.org/abs/2306.06687" target="_blank">Arxiv</a>.
4. VirSci code and data are available for Research community.

## 💡 Run
### Environment

We tested our codebase with PyTorch 2.3.1 and CUDA 12.1. Please install the corresponding versions of PyTorch and CUDA based on your computational resources.

To install the required packages, run:
```bash
pip install -r requirements.txt.
```

### Setup

The raw data is based on the [AMiner Computer Science Dataset](https://www.aminer.cn/aminernetwork).

After preprocessing, the used data is publicly available at [Google Drive](https://drive.google.com/drive/folders/1ZwWMBQ5oK-l4VuzMa60GbMND0g2EIxIu?usp=sharing).

- Past paper database is put in the `Papers/papers.tar.gz`, the corresponding embedding database is put in the `Embeddings/faiss_index.index`.
- Contemporary paper database is put in the `Papers/papers_future.tar.gz`, the corresponding embedding database is put in the `Embeddings/faiss_index_future.index`.
- Author knowledge bank is put in the `Authors/books.tar`.
- Adjacency matrix is put in the `adjacency.txt`.

### Usage

```
python sci_platform/run.py
```

Our code support different collaboration settings. The commonly used arguments:

`--runs`: how many times does the program run

`--team_limit`: the max number of teams for a scientist

`--max_discuss_iteration`: the max discussion iterations for a team in a step

`--max_team_member`: the max team member of a team (including the leader)

`--epochs`: the allowed time steps for one program run (default value is 6, which is enough for a scientist to finish all steps)

### Results

- `{info_dir}/{current_time}_{self.team_name}_dialogue.json` saves the team information: **all team members, selected topic, generated idea and abstract**, where `info_dir` denotes the storage path, `current_time` denotes the start running time, and `self.team_name` is the name of the team.

- `{log_dir}/{current_time}_{self.team_name}_dialogue.log` saves the log record of the team, where `log_dir` denotes the storage path.

## 🙏 Acknowledgements

This project is supported by Shanghai Artificial Intelligence Laboratory.

The multi-agent framework in this work is based on the [AgentScope](https://github.com/modelscope/agentscope).

## 📧 Contact

If you have any questions, please  contact at [chenrenqi@pjlab.org.cn, suhaoyang@pjlab.org.cn].

## ⚖ License

This repository is licensed under the [Apache-2.0 License](LICENSE).

## 📌 BibTeX & Citation

If you find this code useful, please consider citing our work:

```bibtex
Comming soon!
```

