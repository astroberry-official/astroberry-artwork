WEB_ICONS_SIZES := 16 24 32 48 64
ANDROID_ICONS_SIZES := 72 96 144 192
#IOS_1X_SIZES := 20 29 40 76 # No such devices exist anymore
IOS_2X_SIZES := 40 58 80 120 152 167
IOS_3X_SIZES := 60 87 120 180
IOS_ICONS_SIZES := $(IOS_1x_SIZES) $(IOS_2x_SIZES) $(IOS_3x_SIZES)
ALL_ICONS_SIZES := $(WEB_ICONS_SIZES) $(ANDROID_ICONS_SIZES) $(IOS_ICONS_SIZES)

ALL_ICONS := \
	$(ALL_ICONS_SIZES:%=astroberry-icon-%.png) \
	$(ALL_ICONS_SIZES:%=astroberry-icon-white-%.png) \
	astroberry-avatar-500.png \
	astroberry-avatar-white-500.png

all: $(ALL_ICONS)

astroberry-icon-%.png: astroberry-icon.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 48)) "$(lastword $^)" "$@"

astroberry-icon-white-%.png: astroberry-icon-white.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 48)) "$(lastword $^)" "$@"

astroberry-avatar-%.png: astroberry-icon.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 48)) -resize 80%x80% -gravity center -extent $*x$* "$(lastword $^)" "$@"

astroberry-avatar-white-%.png: astroberry-icon-white.svg
	convert -depth 8 -background transparent \
		-density $$(($* * 96 / 48)) -resize 80%x80% -gravity center -extent $*x$* "$(lastword $^)" "$@"

clean:
	rm -f *.png

