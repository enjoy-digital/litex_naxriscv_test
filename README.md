NaxRiscv integration test with LiteX.

[> Run Simulation
-----------------
````
$ litex_sim --cpu-type=naxriscv --with-sdram --sdram-module=MT41K128M16 --sdram-data-width=16 (--trace)
````

[> Build/Run it on Arty
-----------------------
````
$ python3 -m litex_boards.targets.digilent_arty --cpu-type=naxriscv --with-ethernet --build --load
````

[> Build/Run it on Nexys-Video
------------------------------
````
$ python3 -m litex_boards.targets.digilent_nexys_video --cpu-type=naxriscv --uart-name=usb_fifo --with-video-framebuffer --with-sdcard --build --load
````

[> Build/Run it on LiteX-Acorn-Baseboard
----------------------------------------
````
$ python3 -m litex_boards.targets.sqrl_acorn --cpu-type=naxriscv --uart-name=jtag_uart --with-sata --build --load
$ litex_term jtag openocd_xc7_ft232.cfg
````

[> Build/Run it on SDS1104X-E
----------------------------------------
````
$ python3 -m litex_boards.targets.siglent_sds1104xe --cpu-type=naxriscv --with-etherbone --with-video-framebuffer --csr-csv=csr.csv --build --load
$ ping 192.168.1.51
$ litex_server --udp --udp-ip=192.168.1.51
$ litex_term crossover
````