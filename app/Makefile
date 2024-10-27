 .PHONY: clean build-right build-left

clean:
	@rm -rf build

build-right:
	@west build -p -d build/right -S zmk-usb-logging -b nice_nano_v2 -- -DZMK_CONFIG=/Users/hellgod/Projects/zmk-config/config -DSHIELD=splitkb_aurora_sofle_right -DZMK_EXTRA_MODULES=/Users/hellgod/Projects/zmk-config

build-left:
	@west build -p -d build/left -S zmk-usb-logging -b nice_nano_v2 -- -DZMK_CONFIG=/Users/hellgod/Projects/zmk-config/config -DSHIELD=splitkb_aurora_sofle_left -DZMK_EXTRA_MODULES=/Users/hellgod/Projects/zmk-config

full-build: clean build-left build-right
	@cp build/left/zephyr/zmk.uf2 build/left.uf2
	@cp build/right/zephyr/zmk.uf2 build/right.uf2
