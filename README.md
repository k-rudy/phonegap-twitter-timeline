## Twitter Timeline in PhoneGap application

This is a dead simple service that allows to easily integrate an embedded twitter timeline to the PhoneGap native application.

The solution has been tested on PhoneGap 3.1.0 for iOS and Android versions.

### Configuration

1. Create an embedded timeline widget.

    Login to your twitter account --> Settings --> Widgets --> Create new

    After the widget has been created copy it's id either from a RESTful url or from generated *script* block.
    It has the following format:

        410453165654278145

2. Add InAppBrowser PhoneGap plugin to your application.

    If you're using PhoneGapBuild service, add the following to the **config.xml**:

        <gap:plugin name="org.apache.cordova.inappbrowser" />

    If you're using Command Line tools run:

        cordova plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git

3. In your PhoneGap js file open InAppBrowserWindow with the twitter timeline:

        window.open(encodeURI('http://k-rudy.github.io/phonegap-twitter-timeline/?410453165654278145'), '_blank', 'location=no');

4. Replace the widget ID in the url with the id of your embedded widget:


### Troubleshooting

1. If you're using the first version of the service and getting Github 404 Not Found error, you should put slash `/` in front of `?` before your widget id in the widget URL. This is caused by changes in the way Github Pages process parameters. [More Details](https://github.com/k-rudy/phonegap-twitter-timeline/issues/2)

### Working screenshots

![](http://k-rudy.github.io/phonegap-twitter-timeline/images/screenshots.png)


Enjoy!

