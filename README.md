# SDPVO covariance report

Static site with per-keyframe covariance / weight plots produced by the
`duetvo` stereo-DPVO pipeline on M3ED sequences.

**Live site:** https://boragunes.github.io/sdpvo-cov-report/

## Pages

- `index.html` — overview + all summary figures embedded as PDF
- `summary.html` — full text report (rendered from `summary/summary_report.md`)
- `gallery.html` — filterable per-run gallery (sequence × config × run × figure)

## Deploying from scratch

### Option A — browser (no CLI tools needed)
1. Create a new public repo on GitHub named `sdpvo-cov-report` (no README, no .gitignore).
2. In this directory:
   ```bash
   git init -b main
   git add .
   git commit -m "Initial SDPVO cov report site"
   git remote add origin https://github.com/<your-user>/sdpvo-cov-report.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source = "Deploy from a branch" → main / root**, Save.
4. Wait ~1 minute, visit the live URL above.

### Option B — GitHub CLI (`gh`)
```bash
git init -b main
git add .
git commit -m "Initial SDPVO cov report site"
gh repo create sdpvo-cov-report --public --source=. --push
gh api -X POST repos/:owner/sdpvo-cov-report/pages \
    -f 'source[branch]=main' -f 'source[path]=/'
```

## Rebuilding after new runs

From the `duetvo` repo:

```bash
# 1. (if needed) re-run analyzer to refresh figures/CSVs
venv/bin/python eval/analyze_sdpvo_correlations.py sdpvo_multi_results

# 2. re-run summary (CSV aggregation + summary figs)
venv/bin/python eval/summarize_cov_metrics.py sdpvo_multi_results

# 3. rebuild site
venv/bin/python eval/build_report_site.py sdpvo_multi_results --out ../sdpvo-cov-report

# 4. commit + push
cd ../sdpvo-cov-report
git add -A && git commit -m "Refresh plots" && git push
```
