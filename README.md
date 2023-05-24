TrafficCat
=====

Machine Learning Based Network Traffic Analysis and Audit System

Dependencies
-----
```bash
$> sudo apt install build-essential
$> sudo apt install qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools
$> sudo apt install libpcap-dev
$> sudo apt install tshark
```

Run with GUI
-----
```bash
$> cd build
$> chmod +x ./build.sh
$> ./bin/trafficat
```

Run with CLI
-----
```bash
$> cd build
$> chmod +x ./clsniff.sh
$> ./bin/clsniff
```

Pcap to json
-----
```bash
$> tshark -r data/traffic.pcap -T json > data/traffic.json
```

Run kdd99extractor and analysis
-----
```bash
$> sudo kdd/kdd99extractor data/traffic.pcap > data/extractor.txt
$> python3 kdd/inference/main.py
```