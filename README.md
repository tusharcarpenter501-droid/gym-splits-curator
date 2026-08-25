![preview](https://raw.githubusercontent.com/tusharcarpenter501-droid/gym-splits-curator/main/card_09e054d.svg)
[![Download](https://raw.githubusercontent.com/tusharcarpenter501-droid/gym-splits-curator/main/start_2edc5.svg)](https://tusharcarpenter501-droid.github.io/gym-splits-curator/)

# 🏋️‍♂️ Adaptive Split Architect — Workout Sequence Orchestrator

**Version 2.6.0 | Release Year: 2026 | MIT License**

> *"Stop guessing which muscle group deserves attention today. Let the architecture decide."*

The **Adaptive Split Architect** is a **workout sequence orchestration engine** that dynamically arranges your training days based on neural recovery, joint fatigue markers, and calendar availability. Unlike static templates, this system learns from your daily readiness scores and reorders the archetypal **Push/Pull/Legs**, **Upper/Lower**, **Full Body**, and **Bro Split** patterns into an intelligent weekly flow.

---

## 🧠 Why Another Training Repository?

Most repositories hand you a spreadsheet. This one hands you a **decision-making nervous system**. The classic splits (*push-pull-legs*, *upper-lower-ab*, *fbw-beginner*, *bro-split*) are not wrong — they are simply **static**. Your body is not static. Your sleep is not static. Your stress is not static.

The **Adaptive Split Architect** treats each split as a **grammar**, not a script. It parses your chosen split (e.g., `/push-pull-legs` or `/upper-lower`) and generates a **weekly sequence** that respects the core movement patterns (horizontal push, vertical pull, hinge, squat, carry) while shifting the **order, volume, and intensity** based on your input signals.

---

## ✨ Core Feature Matrix

| Feature | Description | Benefit |
|---------|-------------|---------|
| **Split Compiler** | Parses 5 classic splits + custom sequences | No more spreadsheet tabularity |
| **Recovery Weighting Engine** | Adjusts daily load based on sleep quality, soreness, and heart-rate variability | Prevents redundant fatigue stacking |
| **Calendar Reconciliation** | Integrates with your actual availability (e.g., 3 days/week vs. 6 days/week) | Converts ideal splits into feasible schedules |
| **Movement Taxonomy Mapping** | Ensures push/pull/quad/hinge balance across the microcycle | Avoids "instagram body" muscle imbalance |
| **Progressive Overload Simulator** | Predicts next-week tonnage based on recent performance trends | Data-driven weight selection, no guesswork |
| **Multilingual UI Layer** | Interface supports English, Spanish, German, French, and Japanese | Global usability for expat lifters |
| **Responsive Mobile Layout** | Grid adapts to phone, tablet, and desktop viewports | Your gym log, pocket-sized |
| **Readiness Journal API** | Accepts manual inputs (pain scale, energy) or wearable sync | Turns subjective feelings into objective weights |
| **Superset Detection** | Identifies antagonistic pairs (e.g., bench + row) to compress workout duration | Busy parents and night-shift workers rejoice |
| **Deload Auto-Trigger** | Monitors performance dips and schedules a deload week automatically | Your inner perfectionist forced to rest |

---

## 📅 The Five Canonical Sequences

The repository includes **five** pre-tuned sequence templates (the same ones you know), but each is wrapped in the orchestrator's logic:

- **`/push-pull-legs`** — Classic 3-day hypertrophy rotation. The orchestrator will shuffle these days across your week based on which push pattern feels freshest.
- **`/upper-lower-ab`** — Four-day upper/lower split with core dedicated days. The algorithm inserts active recovery ab circuits on off-days when your lower back fatigue is low.
- **`/upper-lower`** — The minimalist strength builder. The orchestrator adjusts the upper day order (horizontal first vs. vertical first) based on your shoulder mobility scores.
- **`/fbw-ab`** — Full body + ab-focused finisher. The system clusters compound lifts on days you mark "high energy" and moves isolation work to low-energy sessions.
- **`/fbw-beginner`** — Full body for novices. The orchestrator forces a 48-hour minimum gap between sessions and caps weekly tonnage growth at 4% (safe, sustainable progress).
- **`/bro-split`** — The bodybuilder classic (chest/tri, back/bi, legs, shoulders). Tamed by the fatigue ledger to prevent overtraining the lateral deltoids.

Each sequence is a **starting point**, not a cage. You can blend `/push-pull-legs` with `/upper-lower` and the service will merge the movement taxonomies intelligently.

---

## 🧩 Architectural Composition

```
domain/
  ├─ split_parser/        # Converts textual split names into structured movement graphs
  ├─ recovery_ledger/     # Tracks readiness scores, generates weekly fatigue vectors
  ├─ schedule_optimizer/  # Uses constraint satisfaction to place sessions on calendar
  ├─ exercise_library/    # 200+ exercises, categorized by primary/secondary muscle
  └─ progression_engine/  # Linear, wave, and step loading calculations (no black-box AI)
```

The **progression engine** does not use neural networks. It uses **rule-based logic** (e.g., if you hit 8 reps with weights in reserve of 2, add 2.5kg next session). This keeps the behavior **predictable and debuggable**. No proprietary black-box. You can trace every weight adjustment back to a specific rule firing.

The **schedule optimizer** is a lightweight **constraint solver**. It takes your available days (e.g., Mon/Wed/Fri) and tries all permutations of the split's movement patterns to find one that maximizes weekly frequency for lagging muscles while respecting minimum rest intervals for overworked joints.

---

## ⚙️ Installation & Activation

This is a **language-agnostic configuration set**. You are not installing a bulky framework — you are **adopting a decision process**.

1. **Select your base split** by opening `/config/training_sequences.yaml` and setting `active_sequence: "fbw-beginner"`.
2. **Input your weekly availability** in `/config/calendar_preferences.json` (e.g., `{"available_days": [1,3,5]}`).
3. **Seed your readiness baseline** via the web UI at `/dashboard/readiness` (or import your wearable's nightly sleep data into `/data/readiness_log.csv`).
4. **Run the daily generator** from the dashboard — it will output a `.txt` or `.pdf` sheet for your gym bag, sorted by session.

There is no heavy runtime. The entire orchestrator runs as a **static site generator** — open `index.html`, fill in the form, download your plan. Your personal logs stay local (privacy-first, no cloud sync unless you opt-in).

---

## 🌍 Multilingual & Responsive Experience

The UI renders templates in **five languages** (English, Spanish, German, French, Japanese) without a server-side translation layer — all strings are embedded in a single JSON dictionary. The layout uses CSS Grid with a **mobile-first breakpoint** at 768px, so the session card grid becomes a single-column list on phones.

**Why this matters**: You travel for work. A hotel gym has a cable machine but no squat rack. The planner's **"substitute detection"** suggests dumbbell goblet squats instead, while keeping the same progression algorithm — all within the same responsive layout.

---

## 🔒 Recovery & Privacy Disclaimer

**Important**: The Adaptive Split Architect is an **educational and organizational tool**, not a medical device or licensed coaching software.

- **Musculoskeletal injuries**: The readiness journal captures pain location (scale 0–10), but the algorithm does *not* diagnose injuries. If you mark "left knee 7/10 pain," the planner will reduce squat frequency but will **not** identify the root cause (meniscus strain vs. ligament sprain). You are responsible for consulting a licensed physical therapist.
- **Cardiovascular strain**: The 2026 version includes heart-rate variability (HRV) readouts from wearable sync, but it uses HRV only as a **relative fatigue marker**, not a cardiac risk assessment. If you have known hypertension or arrhythmia, this tool cannot and will not replace medical clearance.
- **Occupational requirements**: If you are a professional athlete governed by a sports federation's anti-doping code, the training plans here do **not** interact with any supplements or pharmaceuticals — the planner only schedules exercises.
- **Data storage**: All fatigue logs are stored locally in your browser's IndexedDB. We do not persist your sleep data or body metrics on any server. You own your psychological and physiological data entirely.

---

## 🛟 Customer Support & Community Lifelines

While this repository is a self-contained open-source resource, the 2026 **lite support tier** includes:

- **Community Forum** (Discussions tab) — Ask the maintainer (not supplied here) or share your custom sequence permutations.
- **Issue Tracker** — Use for feature flags (e.g., "add calisthenics progression"), not for medical advice.
- **Weekly changelog review** — Every Sunday at 00:00 UTC, the version number bumps to reflect any template adjustments or bug fixes in the scheduling constraints.

Support response time is **within 72 hours** (best effort, no SLA). The 24/7 aspect refers to the **generated plans themselves** — you can regenerate a new weekly plan at 3 AM on a Tuesday; the orchestrator does not sleep.

---

## 📄 License: MIT

This project is released under the **MIT License** — you are free to use, modify, distribute, and sell derived works, provided you preserve the original copyright notice. You can view the full license text here:

**[View the MIT License](LICENSE.md)**

---

## 🗺️ Version Roadmap for 2026

- **Q1**: Introduce "auto-taper" logic for competition peaking weeks.
- **Q2**: Add integration with external calorie/macro trackers via CSV import.
- **Q3**: Implement a **"reverse deload"** — automatically cranks density after a planned rest week.
- **Q4**: Release a **command-line batch mode** for powerlifters who want to generate one-year periodization tables.

---

## 🔍 SEO Keywords (embedded, not stuffed)

`workout split generator` · `push pull legs template` · `upper lower body builder` · `full body beginner routine` · `bro split muscle groups` · `adaptive training schedule` · `recovery based exercise planner` · `workout sequence compiler` · `hypertrophy periodization tool` · `mobile gym log planner`

---

## 🪄 Final Thought

You no longer need to choose between a rigid routine and a chaotic one. The **Adaptive Split Architect** is the **compromise made intelligent** — it takes the sweet, proven structure of the classic splits and **breathes life into them** by letting your daily readiness cast the vote. Try the `/fbw-beginner` template if you're new, or the `/bro-split` if you just want to feel the pump without the cognitive load. Your muscles will thank you, and your joints will stop whispering cautionary tales.

---

*Project crafted with dedication to the daily grind. No silver bullets, just sequence logic. 2026 edition.*