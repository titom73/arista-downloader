# Arista Software Downloader

Script to download Arista softwares to local folder, Cloudvision or EVE-NG.

## scripts

### eos-download

```bash
eos-download -h
usage: eos-download [-h] [--token TOKEN]
    --version VERSION
    [--image IMAGE]
    [--destination DESTINATION]
    [--eve]
    [--noztp]
    [--verbose VERBOSE]

EOS downloader script.

optional arguments:
  -h, --help            show this help message and exit
  --token TOKEN         arista.com user API key - can use ENV:ARISTA_TOKEN
  --image IMAGE         Type of EOS image required
  --version VERSION     EOS version to download from website
  --destination DESTINATION
                        Path where to save EOS package downloaded
  --eve                 Option to install EOS package to EVE-NG
  --noztp               Option to deactivate ZTP when used with EVE-NG
  --verbose VERBOSE     Script verbosity
```

- Token are read from `ENV:ARISTA_TOKEN` unless you specify a specific token with CLI.

- Supported platforms:

  - `INT`: International version
  - `64`: 64 bits version
  - `2GB` for 2GB flash platform
  - `2GB-INT`: for 2GB running International
  - `vEOS`: Virtual EOS image
  - `vEOS-lab`: Virtual Lab EOS
  - `vEOS64-lab`: Virtual Lab EOS running 64B
  - `cEOS`: Docker version of EOS
  - `cEOS64`: Docker version of EOS running in 64 bits

### Cloudvision Image uploader

Create an image bundle on Cloudvision.

```bash
cvp-upload -h
usage: cvp-upload [-h]
    [--token TOKEN]
    [--image IMAGE]
    --cloudvision CLOUDVISION
    [--create_bundle]
    [--timeout TIMEOUT]
    [--verbose VERBOSE]

Cloudvision Image uploader script.

optional arguments:
  -h, --help            show this help message and exit
  --token TOKEN         CVP Authentication token - can use ENV:ARISTA_AVD_CV_TOKEN
  --image IMAGE         Type of EOS image required
  --cloudvision CLOUDVISION
                        Cloudvision instance where to upload image
  --create_bundle       Option to create image bundle with new uploaded image
  --timeout TIMEOUT     Timeout connection. Default is set to 1200sec
  --verbose VERBOSE     Script verbosity
```

## Requirements

Repository requires Python `>=3.6` with following requirements:

```requirements
cvprac
cryptography
paramiko
requests
requests-toolbelt
scp
tqdm
```

## Installation

### Python PIP

```bash
$ pip install git+https://github.com/titom73/arista-downloader
```

### Poetry

```bash
# Install dependencies
poetry install

# Run script
poetry run python <script>
```

## Author

From an original idea of [@Mark Rayson](https://github.com/Sparky-python) in [arista-netdevops-community/eos-scripts](https://github.com/arista-netdevops-community/eos-scripts)

## License

Code is under [Apache2](LICENSE) License
