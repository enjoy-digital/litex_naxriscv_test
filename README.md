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