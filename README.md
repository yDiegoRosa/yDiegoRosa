<div align="center">

<img src="https://raw.githubusercontent.com/yDiegoRosa/yDiegoRosa/main/assets/banner.svg" width="100%" alt="Diego Rosa — AI Engineer"/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=19&duration=3200&pause=900&color=00D9FF&center=true&vCenter=true&width=640&lines=%3E+deploying+model...+latency%3A+38ms+%E2%9C%93;%3E+shipping+ML+systems%2C+not+notebooks;%3E+from+dataset+to+production+endpoint" alt="Typing SVG"/>

<a href="https://www.linkedin.com/in/rdiegosilva"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:diegodg22@outlook.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://yinvictus1.github.io/Curriculum/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=About.me&logoColor=white"/></a>

</div>

<br/>

```console
diego@ai-engineer:~$ whoami --verbose

  role         AI Engineer · Computer Vision & LLM Systems
  location     Rio de Janeiro, Brazil  (UTC-3, full US overlap)
  degree       Systems Analysis & Development — graduating late 2026
  owns         data pipeline → model → API → deployment → monitoring
  cares about  latency, inference cost, failure handling
  status       open to remote roles ▉
```

I build machine learning systems that **run end to end** — not notebooks. Most of my work lives where a model stops being an experiment and starts being a service somebody depends on.

---

## 🧬 How I Ship a Model

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1117','primaryTextColor':'#C9D6E3','primaryBorderColor':'#00D9FF','lineColor':'#00D9FF','secondaryColor':'#101A2B','tertiaryColor':'#0D1117','fontFamily':'Fira Code'}}}%%
flowchart LR
    A[📦 Raw Data] --> B[🧹 Pipeline<br/>clean · augment · split]
    B --> C[🧠 Training<br/>PyTorch · YOLO]
    C --> D{📏 Eval Gate<br/>recall · calibration}
    D -->|fails| C
    D -->|passes| E[⚡ Export<br/>ONNX · quantize]
    E --> F[🚀 Serving<br/>Django / FastAPI]
    F --> G[📊 Monitoring<br/>latency · cost · drift]
    G -.->|drift detected| B
```

---

## 🚀 Selected Work

<table>
<tr>
<td width="50%" valign="top">

### 🦷 CárieScan AI
`computer vision` `healthcare`

Detects dental caries in X-rays and intraoral photos, built to run inside a real clinic workflow.

<img src="https://img.shields.io/badge/YOLO11-00D9FF?style=flat-square&logoColor=0D1117"/> <img src="https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white"/> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>

<details>
<summary><b>⚙️ The hard part</b></summary>
<br/>
Clinic hardware is modest, so inference had to be fast without trading away recall on small lesions. ONNX export plus quantization brought latency down while keeping detection quality on the cases that matter clinically.
</details>

</td>
<td width="50%" valign="top">

### 🩻 Chest X-Ray Anomaly Detection
`deep learning` `medical imaging`

Pipeline for detecting pulmonary anomalies in chest radiographs.

<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/CNN-00D9FF?style=flat-square&logoColor=0D1117"/> <img src="https://img.shields.io/badge/Medical_Imaging-1E2A3A?style=flat-square"/>

<details>
<summary><b>⚙️ The hard part</b></summary>
<br/>
Heavy class imbalance makes accuracy actively misleading — a model predicting "normal" every time scores well and helps nobody. Built an evaluation protocol around the metrics that reflect clinical usefulness instead.
</details>

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📉 DropoutRisk `in progress`
`predictive modeling` `education`

Risk scoring that flags students likely to drop out while there's still time to intervene.

<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white"/> <img src="https://img.shields.io/badge/Calibration-00D9FF?style=flat-square&logoColor=0D1117"/>

<details>
<summary><b>⚙️ The hard part</b></summary>
<br/>
A raw score is useless to a coordinator. The model outputs calibrated probabilities, and the decision threshold is chosen against the real cost tradeoff between missing a student and wasting an intervention.
</details>

</td>
<td width="50%" valign="top">

### 🎥 TrackFlow
`object tracking` `operational analytics`

Multi-object tracking and counting of people and vehicles from video streams.

<img src="https://img.shields.io/badge/YOLO-00D9FF?style=flat-square&logoColor=0D1117"/> <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white"/>

<details>
<summary><b>⚙️ The hard part</b></summary>
<br/>
Identity has to survive occlusion. If a tracker reassigns IDs when objects cross, counting error compounds over a long session until the number is worthless.
</details>

</td>
</tr>
</table>

<div align="center">

**📝 Examina** — production Django platform for exam simulations, running inside an academic institution
<img src="https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>

</div>

---

## 🛠️ Stack

<div align="center">
<table>
<tr>
<td align="center" width="25%">

**Vision & ML**

<img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow,opencv&perline=2"/>

`YOLO` `ONNX`
`scikit-learn`

</td>
<td align="center" width="25%">

**LLM & MLOps**

<img src="https://skillicons.dev/icons?i=docker,githubactions,git,linux&perline=2"/>

`RAG` `evals`
`monitoring`

</td>
<td align="center" width="25%">

**Backend & Data**

<img src="https://skillicons.dev/icons?i=django,fastapi,postgres,mysql&perline=2"/>

`REST APIs`
`pandas` `NumPy`

</td>
<td align="center" width="25%">

**Cloud** *(building on)*

<img src="https://skillicons.dev/icons?i=azure,github&perline=2"/>

`AI Foundry`
`Azure OpenAI`

</td>
</tr>
</table>
</div>

---

## 📊 Activity

<div align="center">

<img height="160em" src="https://github-readme-stats.vercel.app/api?username=yDiegoRosa&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=00D9FF&icon_color=00D9FF"/>
<img height="160em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=yDiegoRosa&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D9FF"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=yDiegoRosa&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=00D9FF&line=00D9FF&point=FFFFFF&area=true&radius=8" width="96%"/>

</div>

---

<div align="center">

## 📫 Let's talk

Always up for a conversation about computer vision, LLM systems, or a hard production problem.

<a href="mailto:diegodg22@outlook.com"><img src="https://img.shields.io/badge/diegodg22@outlook.com-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/rdiegosilva"><img src="https://img.shields.io/badge/rdiegosilva-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=110&section=footer" width="100%"/>

</div>