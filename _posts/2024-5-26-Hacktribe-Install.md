---
layout: post
title: Hacktribe Install
tags:
- Audio
- Electribe
- Hacktribe
---

The Hacktribe is a custom firmware for the electribe 2. It adds additional features including FX and allows the sampler to use oscillators from the synth.<br><br>
Please note this is for demonstration purposes only. Attempting to install the Hacktribe could brick your device.<br><br>
Before attempting the Hacktribe try updating the original Electribe firmware. Running v2.02 makes the Hacktribe install straight-forward.<br><br>
This tutorial requires Python, Git and Pip. Steps to install are included below.<br><br>
The following commands use Python to patch the original Electribe firmware, provided by Korg.<br><br>
I recommend using Ubuntu or Debian if you are unfamiliar with bash and python.<br><br>
<b>Installing Hacktribe:</b><br>
Requirements: Electribe 2 Sampler (v2.02), Ubuntu, SD Card<br>
1: Install prerequisite packages: ```apt-get install -y git wget python3```<br>
2: Download pip install script: ```wget https://bootstrap.pypa.io/get-pip.py```<br>
3: Install pip: ```python get-pip.py```<br>
4: Install required python packages: ```pip install argparse bsdiff4```<br>
5: Clone the hacktribe repository: ```git clone --recursive https://github.com/bangcorrupt/hacktribe.git```<br>
6: Change to hacktribe directory: ```cd hacktribe```<br>
7: Download the original Electribe firmware: ```wget https://cdn.korg.com/us/support/download/files/0b87bcd3112fbb8c0ad7b0f55e618837.zip```<br>
8: Extract the electribe firmware: ```unzip 0b87bcd3112fbb8c0ad7b0f55e618837.zip```<br>
9: Prepare the electribe firmware file for patching: ```mv electribe_sampler_system_v202/SYSTEM.vsb .```<br>
10: Patch the firmware: ```python scripts/e2-firmware-patch.py```<br>
11: List files: ```ls```<br>
12: The above command should output a list of files including: hacked-SYSTEM.vsb<br>
13: Rename the hacktribe firmware: ```mv hacked-SYSTEM.vsb SYSTEM.vsb```<br>
14: Insert the Electribe SD card<br>
15: Copy the new firmware to the Electribe: ```mv SYSTEM.vsb KORG/electribe sampler/System/SYSTEM.VSB```<br>
16: Eject the SD card and insert in Electribe<br>
17: Power on the Electribe and Hacktribe firmware will boot.<br>
<br>
<br>
If you use the Hacktribe please consider donating to <a href="https://liberapay.com/bangcorrupt">Bangcorrupt</a> who created the firmware.<br>
Original repository link is available <a href="https://github.com/bangcorrupt/hacktribe">here</a>.<br>
Tag: Audio, Electribe, Hacktribe