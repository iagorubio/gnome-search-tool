icondir = $(datadir)/pixmaps/gsearchtool
icon_DATA = thumbnail_frame.png 

man_MANS = gnome-search-tool.1

@INTLTOOL_SCHEMAS_RULE@
@INTLTOOL_XML_NOMERGE_RULE@

gsettings_SCHEMAS = org.gnome.gnome-search-tool.gschema.xml
@GSETTINGS_RULES@

gsettingsconvertdir = $(datadir)/GConf/gsettings
gsettingsconvert_DATA = gnome-search-tool.convert

Utilitiesdir = $(datadir)/applications
Utilities_in_files = gnome-search-tool.desktop.in 
Utilities_DATA = $(Utilities_in_files:.desktop.in=.desktop)
@INTLTOOL_DESKTOP_RULE@

EXTRA_DIST = \
	$(icon_DATA) \
	$(man_MANS) \
	org.gnome.gnome-search-tool.gschema.xml.in \
	$(Utilities_in_files) \
	$(Utilities_DATA) \
	gnome-search-tool.convert

CLEANFILES = 				\
	gnome-search-tool.desktop	\
	$(gsettings_SCHEMAS)

disthook:
	cd $(distdir) ; rm -f $(CLEANFILES)
