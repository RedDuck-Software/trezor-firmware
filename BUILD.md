### Pre-requisites:
rustup install nightly

rustup default nightly

rustup component add rust-src --toolchain nightly-x86_64-unknown-linux-gnu

### Build:
git clone --recurse-submodules https://github.com/RedDuck-Software/trezor-firmware.git

cd trezor-firmware

poetry install

poetry shell

  ```
  Spawning shell within ~/..../trezor-firmware/.venv
  . ~/..../trezor-firmware/.venv/bin/activate
  brox@brox-laptop:~/..../trezor-firmware$ . ~/..../trezor-firmware/.venv/bin/activate
  (trezor-firmware-py3.12) brox@brox-laptop:~/..../trezor-firmware$ 
  ```
cd core

make clean

make build_unix

### Test emulator:
./emu.py

### Test hello world with emulator:
trezorctl helloworld say-hello RedDuck -a 3 -d
