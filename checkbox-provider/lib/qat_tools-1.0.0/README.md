# qat-tools

Collection of tools for Intel QAT (Quick Assist Technology)

To list all available devices:

```
sudo qatctl list
```

To show configuration of QAT devices:

```
sudo qatctl status
```

To show only data for a set of counters:

```
sudo qatop  --devices 70:00.0 --counters util_pke
```

To output data in terminal:

```
sudo qatop --record  --devices 70:00.0 --counters util_pke exec_pke
```

To install the package with `venv`:

```
sudo apt install -y python3-venv pip
python3 -m venv qat
source qat/bin/activate
pip install ./
```

The tools need to be run with `sudo` and to do so, the path to the binaries
should be provided:

```
sudo ./qat/bin/qatop
```
