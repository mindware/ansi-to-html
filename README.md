## Ansi to Html

This is a port of the ansi to html converter from [bcat](https://github.com/rtomayko/bcat/blob/master/lib/bcat/ansi.rb) to Javascript.

It has a few additions:

* The constructor takes a second <code>options</code> parameter.
* ANSI codes for setting the foreground or background color to default are handled. Default foreground and background colors can be set with the <code>fg</code> and <code>bg</code> options.
* Newlines are converted to <code>&lt;br/&gt;</code> if the <code>newline</code> option is <code>true</code>

## Usage

	var Convert = require('ansi-to-html');

	var convert = new Convert('\x1b[30mblack\x1b[37mwhite')

	console.log(convert.toHtml());

	/*
		prints:
		<span style="color:#000">black<span style="color:#AAA">white</span></span>
	*/
