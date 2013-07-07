kaltura-embed-angular-directive
===============================

An AngularJS directive to embed a Kaltura video.

Embedding a video
-------------------------------
To embed a video, use

<div id="player" kaltura-player kaltura-options="config">
</div>

Or,

<kaltura-player kaltura-options="config">
</kaltura-player>

The kaltura-options attribute specifies the name of the configuration object for the player.
It should be defined in the scope, for example:

function VideoCtrl($scope) {
    $scope.config = {};
 
    $scope.config.widget = {
        'wid': '_243342',
        'uiconf_id': '2877502',
        'entry_id': '0_uka1msg4',
        'flashvars':{
            'externalInterfaceDisabled': false,
            'autoPlay': true
        }
    };
 
    $scope.config.mw = {
        'Kaltura.LeadWithHTML5': true,
        'debug': false,
        'Mw.XmlProxyUrl': 'http://player.kaltura.com//simplePhpXMLProxy.php',
        'Kaltura.UseManifestUrls': true,
        'Kaltura.Protocol': 'http',
        'Kaltura.ServiceUrl': 'http://cdnapi.kaltura.com',
        'Kaltura.ServiceBase': '/api_v3/index.php?service=',
        'Kaltura.CdnUrl': 'http://cdnbakmi.kaltura.com',
        'Kaltura.StatsServiceUrl': 'http://stats.kaltura.com',
        'Kaltura.IframeRewrite': true,
        'EmbedPlayer.EnableIpadHTMLControls': true,
        'EmbedPlayer.UseFlashOnAndroid': false,
        'Kaltura.LoadScriptForVideoTags': true,
        'Kaltura.AllowIframeRemoteService': false,
        'Kaltura.UseAppleAdaptive': true,
        'Kaltura.EnableEmbedUiConfJs': false,
        'Kaltura.PageGoogleAalytics': 'UA-2078931-34'
    };

The widget object holds the configuration of the Kaltura widget and the mw object holds 
the configuration for Kaltura's HTML5 library (optional).

The following script must be included in the page:
<script type='text/javascript' src="http://player.kaltura.com/mwEmbedLoader.php"></script>

A more detailed description can be found here:
http://www.panda-os.com/blog/2013/07/angularjs-kaltura-embed-directive/

And a fiddle:
http://jsfiddle.net/ron_aharoni/xHD6D/19/light/
