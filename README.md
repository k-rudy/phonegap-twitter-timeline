## Twitter Timeline in PhoneGap application

This is a dead simple service that allows to easily integrate an embedded twitter timeline to the PhoneGap native application.

The solution has been tested on PhoneGap 3.1.0 for iOS and Android versions.

### Configuration

1. Add InAppBrowser PhoneGap plugin to your application.

    If you're using PhoneGapBuild service, add the following to the **config.xml**:

        <gap:plugin name="org.apache.cordova.inappbrowser" />

    If you're using Command Line tools run:

        cordova plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git

2. In your PhoneGap js file open InAppBrowserWindow with the twitter timeline:

        window.open(encodeURI('http://k-rudy.github.io/phonegap-twitter-timeline/?roodyruby'), '_blank', 'location=no');

3. Replace the `roodyruby` in the url with the twitter username / hashtag of the page you want to embed


### Troubleshooting

1. If you're using the first version of the service and getting Github 404 Not Found error, you should put slash `/` in front of `?` before your widget id in the widget URL. This is caused by changes in the way Github Pages process parameters. [More Details](https://github.com/k-rudy/phonegap-twitter-timeline/issues/2)

2. If you are using the second version of the service, you might need to replace `widget_id` with `twitter_page` in the url, as things are way simpler now

### Working screenshots

![](http://k-rudy.github.io/phonegap-twitter-timeline/images/screenshots.png)


Enjoy!
