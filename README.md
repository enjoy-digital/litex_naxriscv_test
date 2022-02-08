NaxRiscv integration test with LiteX.

[> Run Simulation
-----------------
````
$ litex_sim --cpu-type=naxriscv --with-sdram --sdram-module=MT41K128M16 --sdram-data-width=16 --trace
$ gtkwave build/sim/gateware/sim.vcd
````