
# Cosmological Simulations

## LCDM with Dark Matter

Relevant files available:

* `Makefile.Gadget2`: makefile for building Gadget2 for running the simulation;
* `Makefile.N-GenIC`: makefile for building N-GenIC used for generating the initial conditions;
* `ics-lcdm-dm.param`: parameter file for generating the initial conditions;
* `lcdm-dm.param`: parameter file for running the simulation.

Important notes:

* Make sure to fix the `GlassFile` path to your own location if required,
  in `ics-lcdm-dm.param`.

## Running the Simulation

Using the provided `Makefile`, make sure to fix the path for the `Gadget2`
and `N-GenIC` binary files.

To generate the initial conditions:

    $ make ics

To run the simulation:

    $ make sim

