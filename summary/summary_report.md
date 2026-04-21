# SDPVO covariance / weight metric summary

- Runs analyzed: **170** (2 configs × 17 sequences × up to 5 repeats).

## Metric reliability (sorted by median |Spearman r|)

Median, 25%–75% interquartile range, count of per-run correlations. Rule of thumb:  |r| < 0.3 weak,  0.3–0.5 modest,  > 0.5 usable.

| metric | median |r| | IQR | n runs | verdict |
|---|---:|---|---:|---|
| `fusion_max` | 0.343 | 0.198–0.559 | 170 | modest |
| `fusion_combined_sum` | 0.325 | 0.190–0.561 | 170 | modest |
| `fusion_mono_only` | 0.317 | 0.194–0.561 | 170 | modest |
| `fusion_stereo_only` | 0.315 | 0.182–0.537 | 170 | modest |
| `max_eig_pos` | 0.310 | 0.202–0.460 | 170 | modest |
| `cond_pos` | 0.307 | 0.202–0.495 | 170 | modest |
| `fusion_geo_mean` | 0.291 | 0.186–0.544 | 170 | weak |
| `headline_axis_tz` | 0.280 | 0.141–0.421 | 170 | weak |
| `axis_tz` | 0.280 | 0.141–0.421 | 170 | weak |
| `fusion_min` | 0.277 | 0.187–0.543 | 170 | weak |
| `mean_w_stereo_only` | 0.265 | 0.151–0.385 | 170 | weak |
| `smoothed_tr_pos_vs_smoothed_rpe` | 0.262 | 0.134–0.529 | 170 | weak |
| `mean_w_max` | 0.261 | 0.132–0.475 | 170 | weak |
| `headline_axis_ry` | 0.249 | 0.134–0.352 | 170 | weak |
| `axis_ry` | 0.249 | 0.134–0.352 | 170 | weak |
| `mean_w_min` | 0.248 | 0.146–0.411 | 170 | weak |
| `mean_w_geo_mean` | 0.247 | 0.146–0.398 | 170 | weak |
| `mean_w_combined_sum` | 0.238 | 0.146–0.458 | 170 | weak |
| `mean_w_mono_only` | 0.236 | 0.128–0.484 | 170 | weak |
| `headline_axis_ty` | 0.224 | 0.118–0.407 | 170 | weak |
| `axis_ty` | 0.224 | 0.118–0.407 | 170 | weak |
| `tr(Σ_full)` | 0.223 | 0.114–0.449 | 170 | weak |
| `confidence` | 0.222 | 0.114–0.453 | 170 | weak |
| `tr_pos` | 0.222 | 0.114–0.453 | 170 | weak |
| `tr(Σ_pos)` | 0.222 | 0.114–0.453 | 170 | weak |
| `axis_tx` | 0.221 | 0.123–0.401 | 170 | weak |
| `headline_axis_tx` | 0.221 | 0.123–0.401 | 170 | weak |
| `headline_axis_rx` | 0.190 | 0.101–0.257 | 170 | weak |
| `axis_rx` | 0.190 | 0.101–0.257 | 170 | weak |
| `log_det_pos` | 0.175 | 0.106–0.459 | 170 | weak |
| `vol_pos` | 0.175 | 0.106–0.459 | 170 | weak |
| `tr(Σ_rot)` | 0.162 | 0.071–0.274 | 170 | weak |
| `axis_rz` | 0.142 | 0.073–0.257 | 170 | weak |
| `headline_axis_rz` | 0.142 | 0.073–0.257 | 170 | weak |

## Most reliable predictors (median |r| ≥ 0.3)

- **`fusion_max`** — median |r| = 0.343 (IQR 0.20–0.56, n=170)
- **`fusion_combined_sum`** — median |r| = 0.325 (IQR 0.19–0.56, n=170)
- **`fusion_mono_only`** — median |r| = 0.317 (IQR 0.19–0.56, n=170)
- **`fusion_stereo_only`** — median |r| = 0.315 (IQR 0.18–0.54, n=170)
- **`max_eig_pos`** — median |r| = 0.310 (IQR 0.20–0.46, n=170)
- **`cond_pos`** — median |r| = 0.307 (IQR 0.20–0.50, n=170)

## Config comparison (default vs superfast)

| metric | default_s0.5 | superfast_s0.5 | Δ (default-superfast) |
|---|---|---|---|
| `fusion_max` | 0.354 | 0.324 | +0.030 |
| `fusion_combined_sum` | 0.338 | 0.310 | +0.028 |
| `fusion_mono_only` | 0.310 | 0.319 | -0.009 |
| `fusion_stereo_only` | 0.327 | 0.284 | +0.043 |
| `max_eig_pos` | 0.315 | 0.301 | +0.014 |
| `cond_pos` | 0.319 | 0.300 | +0.019 |
| `fusion_geo_mean` | 0.308 | 0.285 | +0.023 |
| `headline_axis_tz` | 0.307 | 0.266 | +0.041 |
| `axis_tz` | 0.307 | 0.266 | +0.041 |
| `fusion_min` | 0.283 | 0.275 | +0.008 |
| `mean_w_stereo_only` | 0.277 | 0.255 | +0.023 |
| `smoothed_tr_pos_vs_smoothed_rpe` | 0.216 | 0.274 | -0.058 |

## Calibration & scaling issues (NEES)

- **default_s0.5** — mean NEES: median=7.94e+05 (p25=3.05e+05, p75=1.28e+06)
  - median NEES: 5.29e+05  (target = 6)
  - underestimation factor (mean NEES / 6): median=132388.6×, max=5.8e+05×
  - tail frac(NEES>12): median=1.000 (chi² target ≈ 0.062)
  - sim3 align scale: median=0.9995, |dev from 1| p95 = 3.438e-02
- **superfast_s0.5** — mean NEES: median=1.00e+05 (p25=4.44e+04, p75=1.77e+05)
  - median NEES: 7.35e+04  (target = 6)
  - underestimation factor (mean NEES / 6): median=16703.8×, max=6.8e+04×
  - tail frac(NEES>12): median=1.000 (chi² target ≈ 0.062)
  - sim3 align scale: median=0.9988, |dev from 1| p95 = 5.677e-02

### Interpretation

- **Σ is under-estimated by roughly `mean NEES / 6`×** (median 3.3e+04×, p95 4.8e+05×).  This is the usual behaviour for BA-Schur covariance on visual-only pipelines: the Hessian captures only the information reported by the matched patches and ignores outlier rejection, front-end gating, and cross-edge dependencies.  **Raw Σ cannot be used in a fusion filter without inflation.**
- **sim3 alignment scale stays within 4.8% of 1** (p95 deviation).  The NEES blow-up is therefore not caused by translation-scale distortion — it is intrinsic under-coverage of the Hessian.  This matters because it means the *shape* of Σ can still be trusted even though the absolute magnitude cannot.
- **Top reliability comes from the fusion_max/fusion_combined_sum/fusion_mono_only family** (leaders: `fusion_max`, `fusion_combined_sum`, `fusion_mono_only`).  Fusion composites (median |r| ≈ 0.32) and shape descriptors like `cond_pos` / `max_eig_pos` (median |r| ≈ 0.24) are **scale-invariant** and outperform raw trace / confidence (median |r| ≈ 0.22).
- **Per-axis σ_d diagonals are axis-matched to |e_d|**, so each axis can be used for a per-component gating rule even when the trace summary looks noisy.  See `headline_axis_*` in the table for axis-wise strength.
- **Config difference is small.**  default vs superfast typically move median |r| by <0.05 (see `fig_config_compare.pdf`), so the choice of metric matters much more than the choice of config.
- **For a downstream fusion system, treat Σ as a *relative* signal only:** use `cond_pos` / `max_eig_pos` / fusion composites as ranking features or rescale Σ per run using an empirical NEES-based inflation factor — do not feed the raw covariance into an EKF.

## NEES by sequence (mean NEES median across runs)

| seq | default_s0.5 | superfast_s0.5 |
|---|---|---|
| falcon_outdoor_day_fast_flight_1 | 3.62e+05 | 5.87e+04 |
| falcon_outdoor_day_penno_trees | 2.08e+05 | 3.08e+04 |
| spot_forest_hard | 1.51e+06 | 2.43e+05 |
| spot_forest_road_1 | 1.28e+06 | 1.79e+05 |
| spot_indoor_building_loop | 3.07e+05 | 4.95e+04 |
| spot_indoor_obstacles | 3.07e+05 | 4.44e+04 |
| spot_indoor_stairs | 1.92e+05 | 1.66e+04 |
| spot_indoor_stairwell | 9.40e+04 | 1.44e+04 |
| spot_outdoor_day_art_plaza_loop | 2.93e+06 | 3.89e+05 |
| spot_outdoor_day_penno_short_loop | 1.09e+06 | 1.55e+05 |
| spot_outdoor_day_rocky_steps | 1.37e+05 | 1.34e+04 |
| spot_outdoor_day_skatepark_1 | 1.71e+06 | 1.84e+05 |
| spot_outdoor_day_skatepark_2 | 1.13e+06 | 1.48e+05 |
| spot_outdoor_day_srt_green_loop | 3.28e+06 | 3.91e+05 |
| spot_outdoor_day_srt_under_bridge_1 | 7.94e+05 | 1.00e+05 |
| spot_outdoor_night_penno_plaza_lights | 8.46e+05 | 1.15e+05 |
| spot_outdoor_night_penno_short_loop | 4.12e+05 | 5.91e+04 |