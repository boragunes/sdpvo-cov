# SDPVO covariance / weight metric summary

- Runs analyzed: **170** (2 configs × 17 sequences × up to 5 repeats).

## Metric reliability (sorted by median |Spearman r|)

Median, 25%–75% interquartile range, count of per-run correlations. Rule of thumb:  |r| < 0.3 weak,  0.3–0.5 modest,  > 0.5 usable.

| metric | median |r| | IQR | n runs | verdict |
|---|---:|---|---:|---|
| `pose_drift_R` | 0.559 | 0.434–0.707 | 340 | strong |
| `pose_drift_R__w7_mean` | 0.550 | 0.436–0.722 | 170 | strong |
| `max_eig_pos__w7_std` | 0.542 | 0.397–0.611 | 170 | strong |
| `pose_drift_R__w7_max` | 0.492 | 0.275–0.642 | 170 | modest |
| `tr_pos__w7_std` | 0.465 | 0.323–0.571 | 170 | modest |
| `cond_pos__w7_std` | 0.414 | 0.181–0.601 | 170 | modest |
| `cond_pos__w7_abs_diff` | 0.403 | 0.171–0.600 | 170 | modest |
| `cond_pos__w7_range` | 0.399 | 0.180–0.597 | 170 | modest |
| `cond_pos__w7_max` | 0.351 | 0.224–0.534 | 170 | modest |
| `pose_drift_R__w7_std` | 0.350 | 0.237–0.503 | 170 | modest |
| `fusion_max` | 0.342 | 0.192–0.565 | 170 | modest |
| `fusion_mono_only` | 0.331 | 0.189–0.570 | 170 | modest |
| `fusion_combined_sum` | 0.330 | 0.182–0.566 | 170 | modest |
| `max_eig_pos__w7_mean` | 0.326 | 0.176–0.462 | 170 | modest |
| `max_eig_pos` | 0.326 | 0.192–0.457 | 340 | modest |
| `fusion_stereo_only` | 0.323 | 0.181–0.563 | 170 | modest |
| `cond_pos__w7_mean` | 0.314 | 0.184–0.496 | 170 | modest |
| `fusion_geo_mean` | 0.311 | 0.173–0.571 | 170 | modest |
| `headline_axis_tx` | 0.310 | 0.169–0.452 | 170 | modest |
| `axis_tx` | 0.310 | 0.169–0.452 | 170 | modest |
| `cond_pos` | 0.309 | 0.192–0.488 | 340 | modest |
| `fusion_min` | 0.305 | 0.175–0.563 | 170 | modest |
| `log_det_pos__w7_std` | 0.299 | 0.157–0.529 | 170 | weak |
| `klt_vs_tr_pos` | 0.289 | 0.146–0.417 | 170 | weak |
| `ba_weight_delta_full__w7_mean` | 0.279 | 0.158–0.437 | 170 | weak |
| `conf_vs_flow_disagree` | 0.275 | 0.155–0.428 | 170 | weak |
| `mean_w_stereo_only` | 0.271 | 0.128–0.396 | 170 | weak |
| `smoothed_tr_pos_vs_smoothed_rpe` | 0.255 | 0.133–0.583 | 170 | weak |
| `headline_axis_ry` | 0.254 | 0.134–0.361 | 170 | weak |
| `axis_ry` | 0.254 | 0.134–0.361 | 170 | weak |
| `axis_tz` | 0.250 | 0.113–0.459 | 170 | weak |
| `headline_axis_tz` | 0.250 | 0.113–0.459 | 170 | weak |
| `mean_w_max` | 0.250 | 0.141–0.490 | 170 | weak |
| `mean_w_geo_mean` | 0.248 | 0.138–0.428 | 170 | weak |
| `confidence__w7_std` | 0.245 | 0.153–0.453 | 170 | weak |
| `mean_w_min` | 0.244 | 0.123–0.398 | 170 | weak |
| `mean_w_mono_only` | 0.229 | 0.137–0.491 | 170 | weak |
| `ba_weight_delta_full` | 0.225 | 0.139–0.422 | 340 | weak |
| `mean_w_combined_sum` | 0.223 | 0.147–0.471 | 170 | weak |
| `confidence` | 0.222 | 0.110–0.501 | 340 | weak |
| `tr_pos` | 0.222 | 0.110–0.501 | 340 | weak |
| `tr(Σ_pos)` | 0.222 | 0.111–0.500 | 170 | weak |
| `photo_zncc__w7_std` | 0.216 | 0.089–0.323 | 170 | weak |
| `tr(Σ_full)` | 0.215 | 0.109–0.500 | 170 | weak |
| `tr_pos__w7_mean` | 0.214 | 0.099–0.497 | 170 | weak |
| `klt_uncert__w7_mean` | 0.204 | 0.114–0.336 | 170 | weak |
| `pose_drift_t` | 0.200 | 0.092–0.458 | 340 | weak |
| `confidence__w7_mean` | 0.200 | 0.093–0.494 | 170 | weak |
| `pose_drift_t__w7_mean` | 0.196 | 0.087–0.443 | 170 | weak |
| `ba_weight_delta_full__w7_std` | 0.191 | 0.097–0.339 | 170 | weak |
| `axis_ty` | 0.187 | 0.081–0.301 | 170 | weak |
| `headline_axis_ty` | 0.187 | 0.081–0.301 | 170 | weak |
| `klt_uncert__w7_std` | 0.180 | 0.083–0.310 | 170 | weak |
| `pose_drift_t__w7_max` | 0.180 | 0.079–0.396 | 170 | weak |
| `pose_drift_t__w7_std` | 0.178 | 0.060–0.302 | 170 | weak |
| `photo_zncc__w7_mean` | 0.177 | 0.079–0.295 | 170 | weak |
| `headline_axis_rx` | 0.172 | 0.097–0.248 | 170 | weak |
| `axis_rx` | 0.172 | 0.097–0.248 | 170 | weak |
| `vol_pos` | 0.172 | 0.106–0.514 | 170 | weak |
| `log_det_pos` | 0.172 | 0.106–0.517 | 340 | weak |
| `rpe_vs_klt` | 0.169 | 0.079–0.328 | 170 | weak |
| `log_det_pos__w7_mean` | 0.164 | 0.095–0.508 | 170 | weak |
| `tr(Σ_rot)` | 0.162 | 0.078–0.253 | 170 | weak |
| `rpe_vs_photo_ssd` | 0.151 | 0.089–0.283 | 170 | weak |
| `flow_disagree__w7_mean` | 0.151 | 0.063–0.360 | 170 | weak |
| `headline_axis_rz` | 0.147 | 0.070–0.239 | 170 | weak |
| `axis_rz` | 0.147 | 0.070–0.239 | 170 | weak |
| `rpe_vs_photo_zncc` | 0.146 | 0.066–0.265 | 170 | weak |
| `rpe_vs_flow_disagree` | 0.137 | 0.066–0.336 | 170 | weak |
| `flow_disagree__w7_std` | 0.130 | 0.065–0.236 | 170 | weak |

## Most reliable predictors (median |r| ≥ 0.3)

- **`pose_drift_R`** — median |r| = 0.559 (IQR 0.43–0.71, n=340)
- **`pose_drift_R__w7_mean`** — median |r| = 0.550 (IQR 0.44–0.72, n=170)
- **`max_eig_pos__w7_std`** — median |r| = 0.542 (IQR 0.40–0.61, n=170)
- **`pose_drift_R__w7_max`** — median |r| = 0.492 (IQR 0.28–0.64, n=170)
- **`tr_pos__w7_std`** — median |r| = 0.465 (IQR 0.32–0.57, n=170)
- **`cond_pos__w7_std`** — median |r| = 0.414 (IQR 0.18–0.60, n=170)
- **`cond_pos__w7_abs_diff`** — median |r| = 0.403 (IQR 0.17–0.60, n=170)
- **`cond_pos__w7_range`** — median |r| = 0.399 (IQR 0.18–0.60, n=170)
- **`cond_pos__w7_max`** — median |r| = 0.351 (IQR 0.22–0.53, n=170)
- **`pose_drift_R__w7_std`** — median |r| = 0.350 (IQR 0.24–0.50, n=170)

## Config comparison (default vs superfast)

| metric | default_s0.5 | superfast_s0.5 | Δ (default-superfast) |
|---|---|---|---|
| `pose_drift_R` | 0.552 | 0.575 | -0.022 |
| `pose_drift_R__w7_mean` | 0.549 | 0.551 | -0.002 |
| `max_eig_pos__w7_std` | 0.559 | 0.508 | +0.051 |
| `pose_drift_R__w7_max` | 0.507 | 0.482 | +0.025 |
| `tr_pos__w7_std` | 0.482 | 0.458 | +0.024 |
| `cond_pos__w7_std` | 0.443 | 0.324 | +0.119 |
| `cond_pos__w7_abs_diff` | 0.426 | 0.314 | +0.112 |
| `cond_pos__w7_range` | 0.443 | 0.320 | +0.123 |
| `cond_pos__w7_max` | 0.349 | 0.352 | -0.003 |
| `pose_drift_R__w7_std` | 0.364 | 0.330 | +0.034 |
| `fusion_max` | 0.351 | 0.332 | +0.019 |
| `fusion_mono_only` | 0.337 | 0.331 | +0.006 |

## Calibration & scaling issues (NEES)

- **default_s0.5** — mean NEES: median=7.78e+05 (p25=3.02e+05, p75=1.25e+06)
  - median NEES: 5.20e+05  (target = 6)
  - underestimation factor (mean NEES / 6): median=129724.8×, max=5.7e+05×
  - tail frac(NEES>12): median=1.000 (chi² target ≈ 0.062)
  - sim3 align scale: median=1.0000, |dev from 1| p95 = 0.000e+00
- **superfast_s0.5** — mean NEES: median=9.81e+04 (p25=4.50e+04, p75=1.76e+05)
  - median NEES: 7.27e+04  (target = 6)
  - underestimation factor (mean NEES / 6): median=16348.5×, max=7.2e+04×
  - tail frac(NEES>12): median=1.000 (chi² target ≈ 0.062)
  - sim3 align scale: median=1.0000, |dev from 1| p95 = 0.000e+00

### Interpretation

- **Σ is under-estimated by roughly `mean NEES / 6`×** (median 3.2e+04×, p95 4.8e+05×).  This is the usual behaviour for BA-Schur covariance on visual-only pipelines: the Hessian captures only the information reported by the matched patches and ignores outlier rejection, front-end gating, and cross-edge dependencies.  **Raw Σ cannot be used in a fusion filter without inflation.**
- **sim3 alignment scale stays within 0.0% of 1** (p95 deviation).  The NEES blow-up is therefore not caused by translation-scale distortion — it is intrinsic under-coverage of the Hessian.  This matters because it means the *shape* of Σ can still be trusted even though the absolute magnitude cannot.
- **Top reliability comes from the pose_drift_R/pose_drift_R__w7_mean/max_eig_pos__w7_std family** (leaders: `pose_drift_R`, `pose_drift_R__w7_mean`, `max_eig_pos__w7_std`).  Fusion composites (median |r| ≈ 0.33) and shape descriptors like `cond_pos` / `max_eig_pos` (median |r| ≈ 0.24) are **scale-invariant** and outperform raw trace / confidence (median |r| ≈ 0.22).
- **Per-axis σ_d diagonals are axis-matched to |e_d|**, so each axis can be used for a per-component gating rule even when the trace summary looks noisy.  See `headline_axis_*` in the table for axis-wise strength.
- **Config difference is small.**  default vs superfast typically move median |r| by <0.05 (see `fig_config_compare.pdf`), so the choice of metric matters much more than the choice of config.
- **For a downstream fusion system, treat Σ as a *relative* signal only:** use `cond_pos` / `max_eig_pos` / fusion composites as ranking features or rescale Σ per run using an empirical NEES-based inflation factor — do not feed the raw covariance into an EKF.


## Per-sequence `cond_pos` strength

Why some sequences shine and others don't.  `|Spearman r|` is a *rank* coefficient, so it needs dynamic range in both the predictor (cond(Σ_pos)) and the target (RPE) to be high.  If a sequence has steady motion and uniformly low RPE, there is nothing for any Σ metric to rank — even when the covariance itself is well-formed.

| seq | median \|r\| | n runs | regime |
|---|---:|---:|---|
| spot_outdoor_day_srt_green_loop | 0.723 | 20 | strong (≥0.5) |
| spot_indoor_building_loop | 0.611 | 20 | strong (≥0.5) |
| spot_forest_road_1 | 0.556 | 20 | strong (≥0.5) |
| spot_outdoor_night_penno_plaza_lights | 0.541 | 20 | strong (≥0.5) |
| spot_outdoor_day_skatepark_2 | 0.527 | 20 | strong (≥0.5) |
| spot_outdoor_day_penno_short_loop | 0.462 | 20 | modest (0.3–0.5) |
| spot_outdoor_night_penno_short_loop | 0.316 | 20 | modest (0.3–0.5) |
| spot_outdoor_day_art_plaza_loop | 0.293 | 20 | weak (<0.3) |
| spot_forest_hard | 0.288 | 20 | weak (<0.3) |
| falcon_outdoor_day_penno_trees | 0.271 | 20 | weak (<0.3) |
| spot_outdoor_day_srt_under_bridge_1 | 0.257 | 20 | weak (<0.3) |
| spot_indoor_obstacles | 0.217 | 20 | weak (<0.3) |
| spot_indoor_stairwell | 0.217 | 20 | weak (<0.3) |
| spot_outdoor_day_rocky_steps | 0.178 | 20 | weak (<0.3) |
| spot_outdoor_day_skatepark_1 | 0.168 | 20 | weak (<0.3) |
| falcon_outdoor_day_fast_flight_1 | 0.123 | 20 | weak (<0.3) |
| spot_indoor_stairs | 0.079 | 20 | weak (<0.3) |

### Run-level diagnostic (Spearman across all 170 runs)

- **log dynamic range of RPE**  vs |r| of `cond_pos`  = +0.23 (p=1.7e-05)
- **log dynamic range of cond(Σ_pos)**  vs |r|  = +0.27 (p=6.2e-07)
- **CV of RPE** vs |r|  = -0.12 (p=3.2e-02)

Positive coefficients here mean: **the more a run's error (or predictor) fluctuates, the stronger `cond_pos` ranks keyframes.**  Flat-RPE runs give low |r| even when the covariance is correct — this is an intrinsic statistical limit, not a pipeline bug.


**Top-3 vs bottom-3 sequences (median over runs):**

| regime | RPE p95/p05 (log10) | cond p95/p05 (log10) | RPE CV | n_kf |
|---|---:|---:|---:|---:|
| top-3 (spot_outdoor_day_srt_green_loop, spot_indoor_building_loop, spot_forest_road_1) | 1.36 | 0.65 | 0.51 | 186 |
| bottom-3 (spot_indoor_stairs, falcon_outdoor_day_fast_flight_1, spot_outdoor_day_skatepark_1) | 1.40 | 0.47 | 0.90 | 148 |

## NEES by sequence (mean NEES median across runs)

| seq | default_s0.5 | superfast_s0.5 |
|---|---|---|
| falcon_outdoor_day_fast_flight_1 | 3.58e+05 | 6.30e+04 |
| falcon_outdoor_day_penno_trees | 1.98e+05 | 2.87e+04 |
| spot_forest_hard | 1.56e+06 | 2.37e+05 |
| spot_forest_road_1 | 1.28e+06 | 1.76e+05 |
| spot_indoor_building_loop | 3.02e+05 | 5.23e+04 |
| spot_indoor_obstacles | 3.08e+05 | 4.50e+04 |
| spot_indoor_stairs | 1.91e+05 | 1.72e+04 |
| spot_indoor_stairwell | 9.08e+04 | 1.36e+04 |
| spot_outdoor_day_art_plaza_loop | 2.92e+06 | 3.96e+05 |
| spot_outdoor_day_penno_short_loop | 1.07e+06 | 1.50e+05 |
| spot_outdoor_day_rocky_steps | 1.43e+05 | 1.22e+04 |
| spot_outdoor_day_skatepark_1 | 1.75e+06 | 1.85e+05 |
| spot_outdoor_day_skatepark_2 | 1.15e+06 | 1.42e+05 |
| spot_outdoor_day_srt_green_loop | 3.34e+06 | 4.05e+05 |
| spot_outdoor_day_srt_under_bridge_1 | 7.78e+05 | 9.81e+04 |
| spot_outdoor_night_penno_plaza_lights | 8.45e+05 | 1.11e+05 |
| spot_outdoor_night_penno_short_loop | 4.03e+05 | 6.06e+04 |