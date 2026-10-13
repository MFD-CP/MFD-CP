## Hi there 👋

<!--
**MFD-CP/MFD-CP** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# Multimodal Fabric Dataset under Controlled Perception (MFD-CP)

## Overview

The Multimodal Fabric Dataset under Controlled Perception (MFD-CP) contains 298 fabric samples. Each sample includes ten multi-view RGB images, temporally aligned measurements collected through controlled robotic exploration, and expert annotations.

Each robotic-exploration trial contains acceleration, six-axis force/torque, two-channel acoustic signals, and GelSight tactile images.

## Dataset Structure

```text
MFD-CP/
├──multi_view_imaging/
│   ├──fabric_001/
│   │   ├──1_1.png
│   │   ├──1_2.png
│   │   ├──...
│   │   └──1_10.png
│   ├──...
│   └──fabric_298/
│       ├──298_1.png
│       ├──298_2.png
│       ├──...
│       └──298_10.png
├──robotic_exploration/
│   ├──fabric_001/
│   │   ├──continuous_pressing/
│   │   │   ├──position_A/
│   │   │   │   ├──orientation_0/
│   │   │   │   │   ├──trial_0/
│   │   │   │   │   │   ├──acceleration.csv
│   │   │   │   │   │   ├──force_torque.csv
│   │   │   │   │   │   ├──audio_main.csv
│   │   │   │   │   │   ├──audio_secondary.csv
│   │   │   │   │   │   └──gelsight_images/
│   │   │   │   │   │       ├──000000.png
│   │   │   │   │   │       └──...
│   │   │   │   │   ├──trial_1/
│   │   │   │   │   └──trial_2/
│   │   │   │   ├──orientation_45/
│   │   │   │   └──orientation_90/
│   │   │   ├──position_B/
│   │   │   ├──position_C/
│   │   │   └──position_D/
│   │   ├──stable_sliding/
│   │   │   ├──track_0_A_to_B/
│   │   │   │   ├──trial_0/
│   │   │   │   │   ├──acceleration.csv
│   │   │   │   │   ├──force_torque.csv
│   │   │   │   │   ├──audio_main.csv
│   │   │   │   │   ├──audio_secondary.csv
│   │   │   │   │   └──gelsight_images/
│   │   │   │   │       ├──000000.png
│   │   │   │   │       ├──000001.png
│   │   │   │   │       └──...
│   │   │   │   ├──trial_1/
│   │   │   │   └──trial_2/
│   │   │   ├──track_1_B_to_A/
│   │   │   ├──track_2_B_to_D/
│   │   │   ├──track_3_D_to_B/
│   │   │   ├──track_4_D_to_C/
│   │   │   ├──track_5_C_to_D/
│   │   │   ├──track_6_C_to_A/
│   │   │   └──track_7_A_to_C/
│   │   └──stable_twisting/
│   │       ├──position_A/
│   │       │   ├──direction_CW/
│   │       │   │   ├──trial_0/
│   │       │   │   │   ├──acceleration.csv
│   │       │   │   │   ├──force_torque.csv
│   │       │   │   │   ├──audio_main.csv
│   │       │   │   │   ├──audio_secondary.csv
│   │       │   │   │   └──gelsight_images/
│   │       │   │   │       ├──000000.png
│   │       │   │   │       └──...
│   │       │   │   ├──trial_1/
│   │       │   │   └──trial_2/
│   │       │   └──direction_CCW/
│   │       ├──position_B/
│   │       ├──position_C/
│   │       └──position_D/
│   ├──fabric_002/
│   ├──...
│   └──fabric_298/
├──expert_annotations.xlsx
├──README.md
├──overview_of_the_298_fabric_samples.png
└──dataset_overview_and_data_acquisition.mp4
```

All components are linked by the zero-padded fabric identifier `fabric_NNN`; for example, `fabric_001` corresponds to record `1` in `expert_annotations.xlsx`. Files within the same `trial_*` directory belong to a common temporally aligned acquisition interval.
