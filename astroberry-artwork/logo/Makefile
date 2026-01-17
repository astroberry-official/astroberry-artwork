SIZES := 600 1200

ALL := \
	$(SIZES:%=astroberry-logo-%.png) \
	$(SIZES:%=astroberry-logo-white-%.png) \
	$(SIZES:%=astroberry-logo-text-%.png) \
	$(SIZES:%=astroberry-logo-text-white-%.png)

all: $(ALL)

astroberry-logo-%.png: astroberry-logo.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 1200)) "$(lastword $^)" "$@"

astroberry-logo-white-%.png: astroberry-logo-white.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 1200)) "$(lastword $^)" "$@"

astroberry-logo-text-%.png: astroberry-logo-text.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 1200)) "$(lastword $^)" "$@"

astroberry-logo-text-white-%.png: astroberry-logo-text-white.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 1200)) "$(lastword $^)" "$@"

clean:
	rm -f *.png

