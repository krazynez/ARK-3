PYTHON=$(shell which python2)

PSPBTCNF_TARGETS = pspbtinf pspbtxnf pspbtnnf pspbtmnf
PSPBTCNF_OBJS = $(addsuffix .bin,$(PSPBTCNF_TARGETS))

.PHONY: clean

all: $(PSPBTCNF_OBJS)

clean:
	$(Q)rm -f $(PSPBTCNF_OBJS)

quiet_cmd_btcnf = BTCNF $<
cmd_btcnf = $(PYTHON) ./btcnf.py build $<

%.bin:%.txt
	@echo $($(quiet)cmd_btcnf)
	@$(cmd_btcnf)

#include ../../../common/make/quiet.mak
include $(PROVITA)/common/make/quiet.mak
