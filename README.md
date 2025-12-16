#🧪 TrialForge - Clinical Retention Simulator**TrialForge** is a predictive analytics concept for clinical trial operations. It models the **Decay of Patient Retention** over time, helping study teams identify high-risk patients and simulate the impact of retention strategies.

It serves as a "What-If" engine for Clinical Operations leaders, demonstrating how proactive interventions (e.g., digital engagement, travel support) can flatten the dropout curve and save millions in trial delays.

##✨ Key Capabilities* **Multifactor Risk Modeling:** Calculates a composite retention probability based on **Engagement Signals** (missed visits), **Protocol Burden** (complex dosing), and **Demographics** (distance to site).
* **Intervention Simulator:** Toggle specific support mechanisms (e.g., *Uber Health Integration*, *ePRO App*) to see their immediate effect on the survival curve.
* **Financial Impact Analysis:** Automatically calculates the potential cost savings of preventing dropouts, based on industry-standard "Cost to Recruit/Replace" metrics.
* **Survival Analysis Visualization:** Uses **Plotly.js** to render a dynamic retention curve against critical study milestones (e.g., "Study End at Month 6").

##🚀 Quick Start1. **Launch:** Open `index.html` in any browser.
2. **Profile Patient:** Use the "Example Patient Profile" to simulate a specific participant (e.g., someone with "Poor" appointment adherence).
3. **Apply Interventions:** Select cards in the "Retention Interventions" section (e.g., *Transportation Support*).
4. **Analyze Outcome:** Watch the "Retention Probability" increase and the "Dropout Timeline" extend.

##🧮 The Math: Retention DecayTrialForge adapts **Exponential Decay** modeling—commonly used in pharmacokinetics—to behavioral retention patterns.

* **P_{baseline}:** Initial probability derived from patient risk factors.
* **k (Dropout Velocity):**
* *Baseline:* High k (Natural attrition due to burden).
* *Intervention:* Low k (Support systems reduce burden).



##⚙️ ConfigurationThe simulation logic is stored in the `EXAMPLE_FACTORS` object. You can adjust these weights to match specific therapeutic areas (e.g., Oncology trials may have different travel burden weights than Dermatology trials).

```javascript
const EXAMPLE_FACTORS = {
    demographic: {
        travel: {
            'local': 0.9,    // Low risk
            'remote': 0.6    // High risk (40% decay penalty)
        }
    }
};

```

##🛠️ Tech Stack* **Frontend:** HTML5, CSS3 (Clinical/Pharma Theme).
* **Logic:** Vanilla JavaScript (ES6+).
* **Charting:** [Plotly.js](https://plotly.com/javascript/).
* **Icons:** [FontAwesome](https://fontawesome.com/).

##⚠️ Disclaimer**Concept Demonstration Only.** The risk algorithms and cost estimates in this tool are illustrative. They are based on general industry averages and should not be used for actual clinical trial management or patient safety monitoring without validation on real-world study data.

##📄 LicenseOpen Source. Intended for educational use and Pre-Sales demonstrations for Clinical Technology platforms.
