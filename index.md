## Firefox tips & optimization

### Firefox Pages


```markdown

about:pages

about: Displays your useragent string
about:about Displays all of the about pages
about:buildconfig Displays configure args
about:cache Lists cache entries
about:compartments Shows JS mem
about:config Displays a settings interface
about:crashes Displays all Firefox crashes
about:healthreport Start up times
about:home Displays the home page
about:memory Shows memory
about:permissions Edit site permissions
about:support Prints all add-ons
about:telemetry Performance and usage
about:mozilla Easter egg
about:robots Easter egg

```

```markdown

### Firefox Tunning

about:config tweaks 

    Turn off the new tab page, and makes it about:blank:
    browser.newtab.url => about:blank

    Turn off Geolocation:
    geo.enabled => false

    Turn off file virus-scan after download:
    browser.download.manager.scanWhenDone => false

    Override the useragent to most common useragent (not needed with Blender/UA Switcher):
    New > string: general.useragent.override =>
    Mozilla/5.0 (Windows NT 6.1; WOW64; rv:20.0) Gecko/20100101 Firefox/20.0

    Force installation of non-updated add-ons:
    New > boolean: extensions.checkCompatibility.[version #] => false

    Disable prefetching (preloading of pages) and DNS prefetching, which lowers RAM usage:
    network.prefetch-next => false
    network.dns.disablePrefetch => false



    Enable HTTP pipelineing regularly, on SSL pages, and on proxies, respectively:
    network.http.pipelining => true
    network.http.pipelining.ssl => true
    network.http.proxy.pipelining => true

    Increase the amount of connections/requests Firefox will make:
    network.http.pipelining.maxrequests => 64
    network.http.max-connections => 512
    network.http.max-persistent-connections-per-server => 32

    Speed up the security delay when installing add-ons:
    security.dialog_enable_delay => 500

    Disable tab animations:
    browser.tabs.animate => false
    browser.fullscreen.animateUp => 0

    Put cache on RAM:
    browser.cache.memory.enable => true
    browser.cache.memory.max_entry_size => -1
    browser.cache.disk.enable => false
    browser.cache.disk.parent_directory => /tmp/firefox

    Reduce page loading delay:
    New > integer: nglayout.initialpaint.delay => 0
    New > boolean: content.interrupt.parsing => true
    New > boolean: content.notify.ontimer => true
    New > integer: content.max.tokenizing.time => 100000
    New > integer: content.notify.backoffcount => -1
    New > integer: content.notify.interval => 100000
    New > integer: content.switch.threshold => 2000000

    Remove submenu slide delay:
    New > integer: ui.submenuDelay => 0

    Set a "do-not-track" header to tell sites not to track browsing habits:
    privacy.donottrackheader.enabled => true

    Disable Pocket, Hello and WebRTC
    loop.enabled => false
    browser.pocket.enable => false
    media.navigator.enabled => false
    media.peerconnection.enabled => false

    Disable Google Blacklists:
    browser.safebrowsing.enabled => false
    browser.safebrowsing.malware.enabled => false

    Disable pings:i
    browser.send_pings => false
    browser.send_pings.require_same_host => true

    Disable suggestions on searchbar:
    browser.search.suggest.enabled => false

    Disable keywords:
    keyword.enabled => false

    Disable certificates:
    browser.ssl_override_behavior => 2

    Disable DNS proxy bypass:
    network.proxy.socks_remote_dns => true

    Disable crash reporting:
    In application.ini in the Firefox folder,
    [Crash Reporter]Enabled=1 => [Crash Reporter]Enabled=0

    For privacy conscious users please check out the following user.js
    https://github.com/crisbrm/user.js
    https://github.com/pyllyukko/user.js
    https://jm42.github.io/compare-user.js/ 
    
    ```
