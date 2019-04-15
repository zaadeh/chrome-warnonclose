On platforms other than Mac, Chrome/Chromium web browser does not offer
an option to warn the user when he tries to close the browser while there
are multiple tabs open. And there doesn't seem to be an official fix
[on the horizon](https://support.google.com/chrome/forum/AAAAP1KN0B0XJE1LBY76g8/).

There are partial remedies like reopening all previously opened tabs on the
next startup using `<Ctrl+Shift+T>` or setting "On Startup" option to
"Continue where you left off". But I still would like to have the
warning on close, for various reasons. There is also a browser extension
which does exactly this.

This small webpage includes the less-than-reputable method of blocking the
web page close event (`window.onbeforeunload`) using JavaScript and asking
for a confirmation. If this page is open in a Chrome/Chromium window (or
any other browser for that matter), you will get the warning whenever
you close the window (or the tab that has loaded this page).

To install, clone this repo on your local system and set the *warnonclose.html*
as the browser home page or open it inside the browser and set the tab
as "pinned". Browsers also require the user to "interact" with this page
before it is allowed to capture this event, so the page needs to be
clicked on (doesn't matter where) or typed in. Output of the page will
indicate whether the hook is in effect.

There are other pages on the internet that do the [same
thing](https://www.maki-chan.de/preventclose.htm), but I was more
comfortable with a page on my local system and under my control for
security/performance reasons.
