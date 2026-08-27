# Live RealSense pose tracking

Run the live Intel RealSense adapter with the hammer mesh, Cutie 2D tracking,
and Kalman filtering:

```bash
conda activate pose
cd ~/jhu/FoundationPose-plus-plus

python test/live_realsense_pose.py \
  --mesh test/mesh/hammer.stl \
  --activate-2d-tracker \
  --activate-kalman-filter
```

The adapter defaults to a `640 x 480` RGB-D stream at `30 FPS`. Press `s` to
select the object ROI, `r` to register it again, and `q` or `Esc` to quit.

Use `--mesh-scale` if the STL units do not already match the physical hammer.
For an STL expressed in millimeters, use `--mesh-scale 0.001` to convert it to
meters.
