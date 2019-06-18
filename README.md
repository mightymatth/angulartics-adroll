## angulartics-adroll

Adroll plugin for [Angulartics](http://github.com/luisfarzati/angulartics).

## Install

[![NPM](https://nodei.co/npm/angulartics-adroll.png)](https://nodei.co/npm/angulartics-adroll/)

First make sure you've read installation and setup instructions for [Angulartics](https://github.com/luisfarzati/angulartics#install).

Then you can install this package either with `npm` or with `bower`.

### npm

```shell
npm install angulartics-adroll
```

Then add `angulartics.adroll` as a dependency for your app:

```javascript
require('angulartics')

angular.module('myApp', [
  'angulartics',
  require('angulartics-adroll')
]);
```

> Please note that core Angulartics doesn't export the name yet, but it will once we move it into [the new organization](http://github.com/angulartics).

### bower

```shell
bower install angulartics-adroll
```

Add the `<script>` to your `index.html`:

```html
<script src="/bower_components/angulartics-adroll/dist/angulartics-adroll.min.js"></script>
```

Then add `angulartics.adroll` as a dependency for your app:

```javascript
angular.module('myApp', [
  'angulartics',
  'angulartics.adroll'
]);
```

## Create Adroll segments

![alt tag](https://help.adroll.com/hc/en-us/article_attachments/204501457/audience_fixed_segment_en-us.gif)

## Track Adroll segments (programmatically)

After creating  Adroll segment, you will get its `segmentId` (e.g. `'d531a9dd'`).

Now you can track the event programmatically.

```javascript
module.controller('SampleCtrl', function ($analytics) {
  $analytics.eventTrack(null, { segments: 'd531a9dd' });
});
```

## Documentation

Documentation is available on the [Angulartics site](https://angulartics.github.io/).

## Development

```shell
npm run build
```

## License

[MIT](LICENSE)
