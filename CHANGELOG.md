# Changelog

## v0.1 — 2026-04-17

Initial release.

### Features
- **`PoseEstimator`** — Estimates 2D camera pose (X, Y, Yaw) from a single video frame using AprilTags with known global positions
- **`CameraCalibration`** — Load camera intrinsics and distortion coefficients from a YAML file
- **`AprilTagMap`** — Define known tag positions and orientations from a JSON file
- **Multi-tag fusion** — Combines pose estimates from multiple simultaneously visible tags using confidence-weighted averaging, with circular mean for yaw
- **Stale pose fallback** — Returns last known pose when no tags are detected, preventing pose discontinuities
- **`camera_calibration.py`** — Interactive camera calibration script using a checkerboard; captures 20 photos and reports RMS reprojection error
- **`live_localization_demo.py`** — Real-time demo with camera feed, tag overlay, and a live top-down map view

### Package
- Installable via `pip install apriltag-pose-estimator`
- Python 3.9+ support
- 60+ unit tests with ≥95% core module coverage
