
MPIEXEC=/usr/local/bin/mpiexec
NP=2
NGENIC=../../N-GenIC/N-GenIC
GADGET2=../../Gadget-2.0.7/Gadget2/Gadget2

help:
	@echo "ics   : generate initial conditions"
	@echo "sim   : run simulation"
	@echo "all   : ics & sim"
	@echo "clean : remove generated files"

ics: ics-lcdm-dm.param
	@mkdir -p ics 
	$(NGENIC) ics-lcdm-dm.param

sim: lcdm-dm.param
	@mkdir -p output
	$(MPIEXEC) -np $(NP) $(GADGET2) lcdm-dm.param

all: ics sim

clean:
	@rm -rf ./ics ./output lcdm-dm.param-usedvalues

