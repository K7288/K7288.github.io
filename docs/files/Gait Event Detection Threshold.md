

# Threshold Desicion Method for Gait Event Detection

Gait events: **heel strike (HS)**, toe strike (TS), heel-off (HO), and **toe-off (TO)**

## 1.[^1]

**Signals**: shank angle(given in the sagittal plane measured counterclockwise with respect to gravity), shank angular velocity, and axial acceleration



acceleration spikes for HS and TO, negative angular velocity during stance, high shank angle at HS, and low shank angle at TO. 

THR detects gait events from observable, physical signal features, where a signal crosses certain thresholds. As can be seen from Fig. 2, the amputee and healthy gaits share the salient characteristics of acceleration spikes for HS and TO, negative angular velocity during stance, high shank angle at HS, and low shank angle at TO. However, the amputee signals have less pronounced features and asmaller shank angle range, so different thresholds for each demographic could be expected. This algorithm, shown in state chart form in Fig. 3, effectively draws “corners” around each gait event and works as follows. For HS, zero-crossing dips in axial acceleration are detected, indicating foot contact. Next, negative angular velocity verifies the front-to-back direction of leg motion, a safety condition. Finally, shank angle must exceed a threshold value, indicating forward shank position and thus HS. Because TO follows a negative spike in axial acceleration, this event is found by identifying increasing acceleration above a negative threshold value. Similarly to HS detection, negative angular velocity is a safety requirement to ensure forward ambulation. Finally, TO is indicated when the shank angle dips below a negative threshold. A total of six threshold parameters were used: one for each signal and gait event combination. Fig. 4 shows a graphical depiction of this algorithm using 70 strides of “normal” data from one healthy subject.

<img src="https://ieeexplore.ieee.org/mediastore_new/IEEE/content/media/10/8541133/8310553/ledou3-2813999-large.gif" style="zoom:50%;" />

> THR state chart. The asterisks denote unique threshold values for transitioning between states, while the arrows indicate increasing or decreasing signal conditions.

Parameter sweeps for a minimum or maximum of a cost function
Visual observation of signals
Priori knowledge

[^1]: D. E. Ledoux, “Inertial sensing for gait event detection and transfemoral prosthesis control strategy,” IEEE Transactions on Biomedical Engineering, vol. 65, no. 12, pp. 2704–2712, 2018.

