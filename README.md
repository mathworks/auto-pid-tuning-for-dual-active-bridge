## Auto PID Tuning For Dual Active Bridge
This model is a demo file showing how to use PIDAutoTuning to obtain the proper PI gain for a Dual Active Bridge converter.
Dual Active Bridges are often used in the following applications because they can be charged bidirectionally and seamlessly while ensuring galvanic isolation. It is often used in the following applications

- Interconversion on different voltage lines in DC microgrids
- Conversion of high voltages (>400V) to 48V or 12V in electric and hybrid vehicles
- Fast chargers for different DC outputs
![B3AEE94E-1F30-46D6-AE3D-E93822F9AE10](https://user-images.githubusercontent.com/62166747/194195458-688b62e0-8b66-4898-a2a5-8a74053b0316.GIF)
![Snag_11d50812](https://user-images.githubusercontent.com/62166747/194195533-081e1062-532d-4ffc-98ad-cb11df038bae.png)

## Setup 
To Run Dual Active Bridge Converte Model:
1. Open Project File.
2. Open Script/DAB_DesignSheet.mlx
3. Edit value of Switching Frequency(Fsw) and Inductance (Ltyp[H])
4. Open TopModel/DualActiveBridgePlant_CurrentCnt.slx("DAB_DesignSheet.mlx" will be run automaticaly )
5. Run Simulation.


To Run PID Auto Tuning Demo:
1. Open Project File.
2. Open Script/DAB_DesignSheet.mlx
3. Edit value of Switching Frequency(Fsw) and Inductance (Ltyp[H])
4. Open TopModel/DualActiveBridge_VpCntWithPIDAutoTuner.slx("DAB_DesignSheet.mlx" will be run automaticaly )
5. Double Click /Controller/Closed-Loop PID Autotuner
6. Enter the desired parameters, referring to this help page. https://jp.mathworks.com/help/slcontrol/ug/tune-pid-controller-in-real-time-using-closed-loop-pid-autotuner-block.html
7. Run Simulation.
8. Automatic PID adjustment is performed at the time timing specified in the Start and Stop blocks.



## The aim of this Demo model
This model shows that the Dual Active Bridge  with Simscape. 
It also shows that Plant transfer function estimation and PID parameter optimization can be performed while the simulation is running.

A power electronic circuit is a system with multiple components, including electrical, control, thermal, and housing design. 
Since a power electronic circuit is a system with multiple components Unlike electrical circuit simulation, system-level simulation that includes multiple elements is possible.

In particular, by linking with the Control System Toolbox, it is possible to perform semi-automation of control design, which does not exist in other companies' electric circuit simulators. 

We believe that this is an effective demo model for those who are troubled by repeated rework at the time of hardware/software integration.

# JAPANESE

## Auto PID Tuning For Dual Active Bridge
このモデルはDual Active Bridgeコンバータに対してPIDAutoTuningで適切なPIゲインを取得することを示すDemoファイルです。
Dual Active Bridgeはガルバニック絶縁を担保しながら双方向かつシームレスに充電が可能であるので
下記のアプリケーションでよく使われます。

- DCマイクログリッドにおける異なる電圧ラインでの相互変換
- 電気自動車・ハイブリッド自動車内の高電圧(400V以上)から48Vもしくは12Vへの変換
- 異なるDC出力に対応する急速充電器

## The aim of this Demo model
このモデルによってSimscapeを用いるとDual Active Bridgeが動作することに加えて、シミュレーションを動かしながら
Plantの伝達関数の推定やPIDのパラメータの最適化が行えることを示すことができます。

パワーエレクトロニクス回路はそのコンポーネント単体で　電気・制御・熱・筐体設計等
複数の要素を持つシステムであるので、
電気回路シミュレーションとは異なり、
複数要素を含めたシステムレベルのシミュレーションが可能です。

特に制御系のToolboxと連携することで他社電気回路シミュレータには存在しない
制御設計の半自動化がこのコンバータでも有効であることが体験できます。

### MathWorks Products (https://www.mathworks.com)

Requires MATLAB release R2022 or newer
MATLAB&reg;/
Simulink&reg;/
Simscape&trade;/
Simscape Electrical&trade;/
Control System Toolbox&trade; /
Simulink Control Design &trade;

## License
The license is available in the License file within this repository
