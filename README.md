# Steven Cleasby-Mayeda

M.S. Artificial Intelligence candidate at Oregon State University, expected June 2027,
with a B.S. in Applied Computer Science, AI focus. I build machine learning systems and
research software, mostly on language-model agents and reinforcement learning, and I am
applying to PhD programs in multi-agent language models.

- Portfolio: https://ancorro.github.io
- LinkedIn: https://linkedin.com/in/stevencm
- Personal email: steven.cleasby.mayeda@gmail.com
- University email: cleasbys@oregonstate.edu
- Location: Corvallis, OR

## Projects

Seven of fourteen. The rest, with figures and write-ups, are at
[ancorro.github.io](https://ancorro.github.io/).

### Humanoid and Robot-Arm Manipulation in Simulation
Isaac Lab, MuJoCo, PPO. Trained a Unitree G1 humanoid to walk to a table, grasp an
object, carry it and set it down, and an SO-101 arm to pick and place from camera input
alone. The learned grasp lifted and held 345 of 360 held-out objects, against 284 for the
previous policy; camera-only placement reached 341 of 400 household objects. Negative
results are kept beside the positive ones, and everything runs in simulation only.

Code: https://github.com/Ancorro/rlRobots

### Learned Routing of Latent State Between LLM Agents
PyTorch, vLLM, Qwen3. Asked whether language-model agents can exchange internal state
instead of text. A reproduction of LatentMAS on Qwen3-4B is bit-identical to the official
code, and a split probe shows the content does cross: 91% with the right KV cache against
92% for text, and 0% with a wrong or absent cache. The latent team only ties a single
agent, +0.1 and -0.2 points, so passing state does not beat one model doing the work.
The latent sender is 19 times faster and uses 2.4 times fewer FLOPs.

Paper draft in progress.

### Deck: Remote Control Distributed Agents
Python, tmux, Rust. Built a web app that runs on each of my computers and gives my phone
a tab per agent session, with one-tap keys for Claude Code, Codex, OpenCode and Pi. Each
agent runs in its own tmux session, so closing the phone or losing signal never stops it.
Linked computers form one Deck with no main host, the phone app fails over after four
seconds, and chats move between hosts mid-conversation. The server listens only on
localhost and new devices pair with a one-time five-minute code.

Code: https://github.com/Ancorro/deck-public

### Reinforcement Learning Control for a Wave Energy Converter
WEC-Sim, PPO, Gymnasium. Wrote a Gymnasium interface that lets reinforcement learning
agents step a full WEC-Sim wave simulation, matching a Simulink-only reference to about
1e-10 in mean power at 19.9 ms per control step. A PPO agent trained on a cheap linear
model transferred with no loss: 148.8 kW on WEC-Sim against 147.4 kW for a tuned damper,
trained in 2.4 minutes instead of 71.

### Computer-Use Agent Evaluated on OSWorld
OSWorld, Claude, Gemma 4. Built an agent that operates a Linux desktop by reading the
screen into numbered items and choosing the next action. On 60 OSWorld multi-app tasks a
plain single-loop design scored 27, ahead of the two-stage planner stacks at 16 and 20;
the difference between those two is within noise at p = 0.42 by an exact McNemar test.
The fast decision model answers in about 0.5 s per step against 5 s for the vision model.

### AI Modeling for HIV Antibody Research
ESM3, LoRA, XGBoost. Predicted broadly neutralizing antibody breadth from heavy-chain
sequence alone on 300 CATNAP antibodies. Frozen ESM3 embeddings raised AUROC from 0.651
to 0.773 over a handcrafted baseline, though the group-bootstrap interval includes zero.
Validation held out all 109 metadata-derived lineages, and a categorical VAE on whole
sequences placed 4 of 4 known VRC34 intermediates correctly.

Project page: https://ancorro.github.io/esm3-banb/

### Guidance: Agentic Field Technician Assistant
Gemini, Python, React. Won first of 20 teams in the beginner track at BeaverHacks 2026,
building a multimodal agent in 24 hours that answers a technician's photo-and-voice
question and draws the next step on the image, with QR-scoped retrieval over equipment
manuals.

Code: https://github.com/ekanshArora123/beaverhacks2026 ·
[Demo](https://lnkd.in/gCfc3Sih) ·
[Submission](https://lnkd.in/gMxyVKYR)

## Experience

**Leading Software Engineer, Waste Treatment Completion Company** (senior capstone,
remote, Sep 2025 to Jun 2026). Led the student team building a Python desktop application
for safety-critical Hanford radioactive-waste vitrification calculations. Architected
validated calculation pipelines for auditability and numerical consistency, ran code
reviews and task delegation, and wrote the developer handover package.
[Project page](https://hlwa-portfolio.github.io/)

**Research Intern, Forever Sabah** (Sabah, Malaysia, Jun to Sep 2023). Analyzed climate
change in Borneo precipitation outliers from weather-model raster data in QGIS, and
designed database schemas for wildlife image datasets supporting individual elephant
re-identification.

**Undergraduate Research Intern, Oregon State University** (Jan to Jun 2023). Wrote data
analysis scripts for research datasets, documented the methodology and presented the
findings at the OSU undergraduate research conference.

## Skills

- Languages: Python, C, JavaScript, SQL
- Machine learning: PyTorch, Hugging Face Transformers, transformer design, training and
  evaluation, ablation studies, LoRA and QLoRA fine-tuning
- Agents: agentic systems, multi-agent orchestration, multimodal pipelines, RAG
- Data: NumPy, pandas, statistics, feature engineering, data cleaning, Weights & Biases
- Systems: Linux, CUDA, Slurm and HPC, Docker, Git
- Web and backend: React, REST APIs, authentication, relational database design
- Practices: testing, CI/CD, code review, technical documentation

## Education

- M.S. Artificial Intelligence, Oregon State University. GPA 3.80, expected June 2027.
  Coursework: Foundation Models, Deep Learning, Optimization for AI, Data Cleaning for
  ML, Graph Theory, Operating Systems II.
- B.S. Applied Computer Science, AI focus, Oregon State University. GPA 3.37, major GPA
  3.52, Honor Roll for 7 terms. June 2026.
