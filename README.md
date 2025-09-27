# AI Sustainability Simulations (Interactive Dashboard)

This repository contains a Jupyter notebook with an interactive dashboard to explore energy, bandwidth, and carbon impacts of AI usage.

## Contents
- `ai_sustainability_dashboard.ipynb` — interactive dashboard with ipywidgets
- `requirements.txt` — minimal dependencies

## Quick Start
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
# Open the notebook and interact with the sliders

## Adjustable Parameters

| Category              | Parameter                | Description                                                                 |
|-----------------------|--------------------------|-----------------------------------------------------------------------------|
| **Demographic**       | Population (millions)    | Scales per-user activity to system-level energy, bandwidth, and emissions. |
| **AI Workflow**       | λ (workflow multiplier)  | Average number of sub-calls/agent steps per request.                        |
|                       | AI growth rate (%/yr)    | Annual growth in per-user request intensity.                                |
| **Optimization**      | Energy efficiency (%)    | Reduction applied to energy vs. baseline scenario.                          |
|                       | Bandwidth efficiency (%) | Reduction applied to bandwidth vs. baseline scenario.                       |
|                       | Infrastructure loss (%)  | Transmission/processing overheads applied to energy baseline.               |
| **Sustainable Solutions** | Edge AI adoption (%) | Adoption of edge/offline inference approaches.                              |
|                       | SLM adoption (%)         | Adoption of small/lightweight language models.                              |

The dashboard updates four panels in real time: **Daily Energy (GWh/day)**, **Daily Bandwidth (EB/day)**, **Workflow Multiplier Effect**, and **Annual CO₂ (kt/year)**, plus prints **2030 projections**.

**Default values:**
- Population: 600 M
- λ: 10
- AI growth: 16%/yr
- Energy eff.: 40%
- Bandwidth eff.: 50%
- Infra loss: 30%
- Edge AI adoption: 20%
- SLM adoption: 30%
