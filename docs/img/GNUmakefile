SIZES := 32 128 152 167 180 192 196
PNGS := $(foreach size,$(SIZES),favicon-$(size).png)
TARGETS := $(PNGS) favicon.ico

.PHONY: all
all: $(TARGETS)

.PHONY: clean
clean:
	rm -f $(TARGETS)

favicon-%.png: cuddlyferris.png
	convert $< -resize $*x$* $@

favicon.ico: $(PNGS)
	icotool -c -o $@ $^
