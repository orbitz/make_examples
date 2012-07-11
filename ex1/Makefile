SUBDIRS = s1 s2 s3
SUBDIRS_TEST = $(patsubst %,%_test,$(SUBDIRS))

.PHONY: all $(SUBDIRS) $(SUBDIRS_TEST)

all: $(SUBDIRS)

$(SUBDIRS):
	$(MAKE) -C $@

$(SUBDIRS_TEST):
	$(MAKE) -C $(patsubst %_test,%,$(@)) test


test: $(SUBDIRS_TEST)
