Keymapper

help users quickly check the key bindings that have been defined `keymapper` **guide** helps users quickly check the key bindings that have been defined to perform different operations on the `Leaflet` overlays (images). With respect to `src/edit/tools/DistortableImage.Guides.js`, let's go through the process of creating one step-by-step.

- Define a `dom_string` (variable name can differ), that'll hold the the basic `HTML` layout of our guide.
- Append this variable to the `guide_strings` for rendering.
- Finally specify a `addToolbar(<map>,<position>,<parent el>,<class>,<guide>)` (see example below) method in `DistortableImage.Edit.js`'s guides collection.

```js
addToolbar(overlay._map, "topright", "div", "l-container", L.DistortableImage.Guides[i])
```  
```js
			/* define guides here */

			// keymapper guide
			addToolbar(overlay._map, "topright", "div", "l-container", L.DistortableImage.Guides[0]);

      /* ------------------ */
```
***

**Note:** The default `toolbarType` will initially be set to "Popup", unless specified otherwise when initializing the image. For eg.,

```js
 img = L.distortableImageOverlay(
        'example.png', {
          // add a toolbarType field with values 'popup' (default) or 'control'
          toolbarType: 'control',
          corners: [
            new L.latLng(51.52,-0.10),
            new L.latLng(51.52,-0.14),
            new L.latLng(51.50,-0.10),
            new L.latLng(51.50,-0.14)
          ],
          fullResolutionSrc: 'large.jpg'
        }
      ).addTo(map);
```
***
