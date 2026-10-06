# TEST 90.3 demos

Fake station site for Spinitron. GitHub Pages: [www.testradio.org](https://www.testradio.org/).

## Custom layout (WWW)

[www.testradio.org](https://www.testradio.org/) — `index.html`

On-air and Programs wrap Spinitron public pages in `custom-layout.html` (`{{SPINITRON_CONTENT}}`, `?layout=1`) on the CNAME `programs.testradio.org`. Forum: [custom layout](https://forum.spinitron.com/t/custom-page-layout/51).

## Listener app (LAF)

[www.testradio.org/spa.html](https://www.testradio.org/spa.html)

Similar but outbound links go to Spinitron's [listener app](https://forum.spinitron.com/t/spinitron-listener-app-listen-to-radio-streams-while-browsing-playlists-schedules-etc/1820).

Links to the listener app go to `STATION.q.spinitron.com`, e.g. `wzbc.q.spinitron.com`. If your station has spaces in its Spinitron ID, use hephens.

You can add query params `laf_css` and `return_url`. Use `laf_css` to link a custom stylesheet and `return_url` is how the visitor navigates back to your web site from the listener app. Both must be percent encoded. For example:

```
https://test.q.spinitron.com/?laf_css=https%3A%2F%2Fwww.testradio.org%2Ftestradio.css&return_url=https%3A%2F%2Fwww.testradio.org%2Fspa.html
```

The listener app has a number of named stock stylesheets which you can select with query param `laf`. `testradio` is one of the stock, see [docs](https://forum.spinitron.com/t/spinitron-listener-app-listen-to-radio-streams-while-browsing-playlists-schedules-etc/1820#p-3748-look-and-feel-laf-11) for the others.

```
https://test.q.spinitron.com/?laf=testradio&return_url=https%3A%2F%2Fwww.testradio.org%2Fspa.html
```

`testradio.css` on this host is the https file `laf_css` fetches.
