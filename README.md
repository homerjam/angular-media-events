# Angular Media Events

This library should introduce angular directives that respond to [events on media objects][1].

#### Supported Events

This list should grow as time goes on.

* [loadedmetadata][2] ([example][3])
* [progress][6] ([example][5])

## Setup

#### Installing

```
bower install angular-media-events
```

#### Including

```js
<script src="/bower_components/angular-media-events/dist/media-events.js"></script>
<script src="/bower_components/angular-media-events/dist/media-events.min.js"></script>
```

#### Using in Angular

```js
angular.module('test', ['media-events']);
```

##Events

#### loadedmetadata

* **available params** (in template):
  * anything in the scope
  * `$event` (jqlite/jQuery Event object)
  * `attrs`
    * `width`
    * `height`

```html
  <video
    ng-src="https://path/to/source"
    loaded-metadata="someFunction($event, attrs)" />
```

#### progress

* **available params** (in template):
  * anything in the scope
  * `$event` (jqlite/jQuery Event object)
  * `attrs`
    * `buffered`

```html
  <video
    ng-src="https://path/to/source"
    progress="someFunction($event, attrs)" />
```

## Conributing

Please feel free to contribute. Checkout [the guidelines][4]. I'm pretty responsive, if I say so myself, so hit me up.

[4]: https://github.com/vernak2539/angular-media-events/blob/master/CONTRIBUTING.md
[1]: https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Media_events
[3]: #loadedmetadata
[5]: #progress
[2]: https://developer.mozilla.org/en-US/docs/Web/Events/loadedmetadata
[6]: https://developer.mozilla.org/en-US/docs/Web/Events/progress
