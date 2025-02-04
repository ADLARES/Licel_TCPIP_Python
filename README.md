# **Licel_TCPIP Python**  

**The Licel_TCPIP python library was developed and tested with python 3.10.11 .** 

**running this library with python version 3.8 will result in error** 

## Installing requirements: 
```shell
pip install -r requirements.txt
```

## run `sampleAcquis.py` example: 
```shell
python sampleAcquis.py --ip <ip> --port <port> --device <Tr address> --memory <memory>
                    --bins <number of bins to read> --sqd_bins <number of sqd bins to read>
                    --range 100mV --squared|no-squared
```

The `sampleAcquis.py` will acquire data through command socket and save data respectively to 
`analogueData.txt`, `analogueSqdData.txt`, `photon.txt` and `photonSQD.txt`


## run `powermeter_example.py`: 
```shell
python3 powermeter_example.py --ip <ip> --port <port>  --acq <num acquis> --channel <channel>
```

the `powermeter_example.py` will demonstrate the use of the push acquistion as well as the 
single trace acquisition. 

## run `pmt_example.py`: 
```shell
python3 pmt_example.py --ip <ip> --port <port> --device <device address> --voltage <voltage>
```

the `pmt_example.py` demonstrate how to list all installed pmt, set and read voltage from a selected device

## run `mpush.py`:
```shell
python3 mpush.py --ip <ip> --port <port>  --acq <num acquis> --shots <num shots>
                 --acquis_per_file <acquis per file> --log
```

`mpush_example.py` demonstrate the use of mpush mode to read multiple datasets from multiple transient recorders, at the same time. 

## Install as module:
#### Execute the following: 
```shell
pip install build
python -m build
pip install -e .
```
