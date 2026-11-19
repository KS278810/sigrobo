# Third-party and reused files of the web screen

| File | Source | Licence |
|---|---|---|
| `static/index.html` (CSS and skeleton), `static/lib.js`, `static/strings.js`, `static/app.js`, `static/live.js`, `static/result.js`, `static/start.js` | adtool (`adtool/web/static` @2c6a2c6), which is built on SurRobo; both by the same author | The author (the user of this project) owns SurRobo and adtool and allowed their use in SigRobo (2026-10-16). SurRobo is marked CC BY-NC 4.0 for others |
| Chakra Petch, IBM Plex Mono (embedded as base64 woff2 in `static/index.html`) | Chakra Petch Project Authors / IBM Plex Project Authors | SIL Open Font License 1.1 (`static/fonts/OFL-*.txt`) |
| `static/vendor/uplot/*` (uPlot 1.x, copied from adtool `static/vendor/uplot`) | Leon Sorokin | MIT (`static/vendor/uplot/LICENSE`) |
| `static/img/robot_*.gif`, the mascot robot09_turquoise: still image by Qwen-Image-Edit-2511, motion by Wan 2.2 I2V-A14B, background removed by the author's own keyer, no MiniMax H3 file | https://huggingface.co/Qwen/Qwen-Image-Edit-2511 and https://huggingface.co/Wan-AI/Wan2.2-I2V-A14B, read on 2026-11-10 | Apache-2.0 for both models |
| `static/img/favicon.svg` | the robot mascot of this workspace (via adtool) | internal asset, same author |
| `static/sample_*.csv` | generated for SigRobo, synthetic data | — |

The files above are adtool's with the changes SigRobo needs. `static/chart.js` (the loss curve, one y axis) is `AD.lossChart` of adtool's `chart.js` (@41e3e6f), the same author. `static/vendor/uplot/` is uPlot by Leon Sorokin, MIT (its `LICENSE` is kept).
Japanese text uses the fonts of the viewer's system; no Japanese font is bundled.

# Third-party material of the browser build

The browser build bundles Pyodide and the wheels below in `vendor/pyodide/` and serves them itself. They come unchanged from the Pyodide 0.28.0 distribution, fetched by `_shared/publish/fetch_vendor.py` with sha256 checks. Each licence file stays inside its wheel.

| Part | Source | Licence |
|---|---|---|
| Pyodide 0.28.0 | https://pyodide.org, source of the MPL files at https://github.com/pyodide/pyodide, tag 0.28.0 | MPL-2.0, text in `licenses/Pyodide-MPL-2.0.txt` |
| The Python standard library in `python_stdlib.zip` | https://www.python.org | PSF License, text in `licenses/CPython-PSF-3.13.txt` |
| numpy 2.2.5, scipy 1.14.1, pandas 2.3.0 and scikit-learn 1.7.0 | the Pyodide 0.28.0 distribution | BSD-3-Clause |
| statsmodels 0.14.4 with patsy 1.0.1 | the Pyodide 0.28.0 distribution | BSD-3-Clause and BSD-2-Clause |
| lightgbm 4.6.0 | the Pyodide 0.28.0 distribution | MIT |
| joblib 1.4.2, threadpoolctl 3.5.0, packaging 24.2, python-dateutil 2.9.0.post0, pytz 2025.2, six 1.17.0 and pyyaml 6.0.2 | the Pyodide 0.28.0 distribution | BSD-3-Clause, Apache-2.0 or BSD, MIT and the dual licence of python-dateutil |
| OpenBLAS 0.3.26, `openblas-0.3.26.zip` | https://github.com/OpenMathLib/OpenBLAS | BSD-3-Clause, text in `licenses/OpenBLAS-BSD-3-Clause.txt` |
| terser, javascript-obfuscator and python-minifier, used by `_shared/publish` to make the public copy and not part of it | npm and PyPI | BSD-2-Clause, BSD-2-Clause and MIT |
