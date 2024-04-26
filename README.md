## Build locally

Install ZMK toolchain:
https://zmk.dev/docs/development/setup

Build the config from the ZMK folder (make sure to clean the `build/` folder before each build):

Left side:  

```sh
west build -s app/ -d build/ -b "nice_nano_v2"  -- -DZMK_CONFIG=/home/mwu/Documents/git-repos/lily58-wireless-zmk-config/config/ -DSHIELD="lily58_left"
cp build/zephyr/zmk.uf2 ../lily58-wireless-zmk-config/build/lily58_left-nice_nano_v2-zmk.uf2
```

Right side:  

```sh
west build -s app/ -d build/ -b "nice_nano_v2"  -- -DZMK_CONFIG=/home/mwu/Documents/git-repos/lily58-wireless-zmk-config/config/ -DSHIELD="lily58_right"
cp build/zephyr/zmk.uf2 ../lily58-wireless-zmk-config/build/lily58_right-nice_nano_v2-zmk.uf2
```
