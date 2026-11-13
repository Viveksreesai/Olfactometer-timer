# Four-Arm Olfactometer Timer

A simple, free, browser-based timer for **single-choice four-arm olfactometer bioassays** in insect behaviour and chemical ecology studies. It records how long an insect spends in each arm and how many times it enters each arm. It can be used in place of older Windows software such as Olfa, which no longer runs on Windows 10/11.

🔗 **Use it online:** https://viveksreesai.github.io/Olfactometer-timer/

---

## Features

- Works in any modern browser (Chrome, Edge, Firefox) on Windows, Mac, Linux or a phone
- Nothing to install, and it also works **offline** (download `index.html` and double-click it)
- Keyboard or click/tap recording
- Records, for each replicate:
  - Time spent (s) in each of the 4 arms and in the centre
  - Number of entries into each arm
  - Time in the treated arm vs the **mean of the 3 control arms**
  - First arm chosen (treated / control) and latency to first choice
- **Undo** for wrong key presses
- Results table that collects all replicates, with **Save as CSV** and **Copy for Excel**

## How to use

1. Enter the **treatment / sample name**, **replicate number**, **duration** (default 600 s = 10 min) and select the **treated arm**.
2. Release the insect into the centre of the arena and press **Start** (or the **Space** bar).
3. While the timer runs, press:

   | Key | Action |
   |---|---|
   | `1` `2` `3` `4` | Insect enters Arm 1, 2, 3 or 4 |
   | `0` | Insect returns to the centre |
   | `Space` | Start / pause |
   | `Backspace` | Undo the last key press |

   You can also click or tap the arm boxes on screen.
4. The timer stops automatically at the set duration (or press **Stop & save**). The replicate is added to the results table and the replicate number moves up by one.
5. When you have finished, click **Save as CSV** (opens in Excel or R) or **Copy for Excel** and paste the results.

> ⚠️ Results are stored only in the browser you are using. They are not uploaded anywhere. **Save a CSV after every session**, especially if you switch computers.

## Output columns

| Column | Meaning |
|---|---|
| Treatment, Rep, Treated arm | Details you entered |
| Arm1–Arm4 (s) | Time spent in each arm |
| Centre (s) | Time spent in the centre (no choice) |
| Arm1–Arm4 entries | Number of entries into each arm |
| Treated time / Mean control time | Treated arm vs average of the 3 control arms |
| Treated entries / Mean control entries | Same comparison, for entries |
| First arm, First choice | First arm entered and whether it was treated or control |
| Latency | Time (s) until the first arm entry |

## Suggested bioassay protocol

- One arm receives the test sample (e.g. 10 µL headspace extract on filter paper); the other three receive the solvent control (e.g. hexane).
- Allow the solvent to evaporate (~30 s) before placing the strips in the arms.
- Keep the airflow equal in all arms. Use charcoal-filtered, humidified air.
- Use each insect only once. Rotate the olfactometer 90° every few replicates to avoid position bias.
- Run a **blank** (solvent in all four arms) to check the setup has no arm bias.
- Typical analysis: **paired t-test** (or Wilcoxon) for treated vs mean control time; **one-way ANOVA + Tukey** for comparing treatments; **chi-square** for first-choice data.

## Citation

If you use this tool in your research, please cite it as:

> Vivek Sree Sai G (2026). *Four-Arm Olfactometer Timer* [Software]. GitHub. https://github.com/Viveksreesai/Olfactometer-timer

## Author

Developed by **Vivek**, PhD scholar (Entomology), Semiochemical Laboratory, Division of Crop Protection, ICAR-Indian Institute of Horticultural Research (IIHR), Bengaluru, India.

Suggestions and bug reports are welcome. Please open an **Issue** in this repository.


