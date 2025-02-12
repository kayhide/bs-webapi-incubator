
### 0.15.5 - (2019-10-09)
* Added `keypress` event handler API
* Added `selectionchange` event handler API
* Added `Text.ofNode`

### 0.15.4 - (2019-09-02)
* Added `Selection.setBaseAndExtent`

### 0.15.3 - (2019-08-22)
* Added `NodeList.forEach`
* Added `Node.asNode`

### 0.15.2 - (2019-05-25)
* Added `File.size`

### 0.15.1 - (2019-05-17)
* Added `URLSearchParams.forEach`
* Added `Element.scrollBy` and `Element.srollByWithOptions`

### 0.15.0 - (2019-05-11)
* (Breaking) Changed `DomRect` coordinates to use `float` instead of `int`

### 0.14.4 - (2019-05-04)
* Added `File.name`

### 0.14.3 - (2019-04-28)
* Added `width`, `height`, `setWidth` and `setHeight` to `CanvasElement`

### 0.14.0 - (2019-04-15)
* Removed deprecated `Webapi.Dom.onload` function
* Removed deprecated `Webapi.File.Url` module alias
* Restructured internal module layout (non-breaking for modules accessed through the `Webapi` top-level module, but breaking if internal `*Re` modules have been accessed directly)
* Enforce private modules (effectively a formality and non-breaking)

### 0.13.6 - (2019-03-22)
* Added `HtmlElement.focusPreventScroll`
* Refined return type of `Node.cloneNode` and `Node.cloneDeepNode` so it now returns the specific type of the cloned node.

### 0.13.5 - (2019-03-15)
* Added `Element.scrollTo`, `Element.scrollToWithOptions`

### 0.13.4 - (2019-02-24)
* Added `URLSearchParams.makeWithDict` and `URLSearchParams.makeWithArray`

### 0.13.3 - (2019-02-19)
* Added `bs.return nullable` to `URLSearchParams.get` since it returns `null`, not `undefined` and therefore does not autmatically conform to the runtime representation of `option` as previosuly assumed.

### 0.13.2 - (2019-01-16)
* Fixed signature of `NamedNodeMap.toArray`, which returned `element` but should return `attr` (considere non-breaking since it was just plain wrong)
* Added `add...` and `removePopStateEventListener` to `Window`
* Added `add...` and `remove...` functions for touch and animation event listeners to `EventTarget`

### 0.13.1 - (2018-11-11)
* Added `add...` and `remove...` functions for drag event listeners to `EventTarget`

### 0.13.0 - (2018-10-09)
* (Breaking) Requires bs-platform > 4.0.0
* (Breaking) Changed `FocusEvent.relatedTarget` to return `option`
* Added `HtmlFormElement` and `HtmlInputElement`

### 0.12.0 - (2018-09-16)
* (Breaking) Fixed return type if `StorageEvent.oldValue` and `StorageEvent.newValue`. They should be `nullable`, but were not.
* Added `Url` and `UrlSearchParams`
* Deprecated `Webapi.File.Url` in favor of `Webapi.Url`

### 0.11.0 - (2018-08-02)
* `EventTarget.dispatchEvent` now take a `Dom.event_like(_)` instead of just `Dom.event`, so it will accept any event subtype.
* `Window.pageXOffset`, `pageYOffset`, `scrollX`, `scrollY`, `scrollLeft` and `scrollTop` now return `float`s instead of `int`s, and `Window.scroll`, `scrollBy`, `scrollTo`, `setScrollLeft` and `setScrollTop` take `float`s instead of `int`s
* `HtmlElement.offsetParent` now returns an `option`
* `Selection.anchorNode` and `Selection.focusNode` now return `option`s
* `Element.closest` now returns an `option`

### 0.10.0 - (2018-06-14)
* Added inheritance of `HtmlElement` and its ancestors to `HtmlImageElement`
* Deprecated `HtmlImageElement.onload`
* Fixed inconsistencies with `HtmlImageElement.src` and `HtmlImageElement.getSrc`, breaking the API
* Fleshed out `HtmlImageElement`

### 0.9.1 - (2018-04-19)
* Renamed `Document.docType` to `Document.doctype` to fix #95

### 0.9.0 - (2018-04-17)
* Support `bs-platform@3.0.0`. If your app isn't using that version, then don't upgrade to `0.9.0`; otherwise, please do!

### 0.8.0 - (2018-01-03)
* Added `EventTarget.unsafeAsDocument`, `EventTarget.unsafeAsElement` and `EventTarget.unsafeAsWindow` functions
* Removed deprecated `Bs_webapi` module`
* Added event-specific listener APIs to `EventTarget`, e.g. `EventTarget.addMouseMoveListener(mouseEvent => ...)`
* Added `requestCancellableAnimationFrame` and `cancelAnimationFrame`
* Fixed msising `@bs.return` annotations causing type unsoundness
* Fixed typo in encoding of `insertPosition` type
* Added `Dom.HtmlImageElement`, `File` and `File.Url`
* Fixed `HtmlElement.offsetParent` returning `int` instead of `Dom.Element`

### 0.7.0 - (2017-09-22)
* Added `Webapi` module, Deprecated `Bs_webapi`
* Removed deprecated Storage API
* Add `Document.unsafeAshtmlDocument`, `Element.unsafeAsHtmlElement`. Deprecated `Document.asHtmlDocument`, `Element.asHtmlElement`, `HtmlEleement.ofElement`.
* Changed `Dom.history` and `Dom.location` to use `window` instead of `document`

### 0.6.1 - (2017-09-10)
* Fix incorrect heuristic in `HtmlElement.ofElement`

### 0.6.0 - (2017-09-10)
* Renamed createText to CreateTextNode, according to spec
* Deprecated Storage API, it's been upstreamed to `bs-platform` as `Dom.Storage`
* Removed `ReasonJs`  namespace. Use ` Bs_webapi`  instead
