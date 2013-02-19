ANOLIS = anolis

all: Overview.html

Overview.html: Overview.src.html data Makefile
	$(ANOLIS) --output-encoding=ascii --omit-optional-tags --quote-attr-values \
	--w3c-compat --enable=xspecxref --enable=refs --w3c-shortname="alarm-api" \
	--w3c-status=ED --filter=".publish, .now3c" $< $@

publish: Overview.src.html data Makefile
	$(ANOLIS) --output-encoding=ascii --omit-optional-tags --quote-attr-values \
	--w3c-compat --enable=xspecxref --enable=refs --w3c-shortname="alarm-api" \
	--filter=".dontpublish" --pubdate="$(PUBDATE)" --w3c-status=ED \
	$< Overview.html
