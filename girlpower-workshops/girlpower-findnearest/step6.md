# Create a new hexagon layer

Open the index.js file `src/index.js`

[Link to Deck.gl documentation](https://deck.gl/#/documentation/submodule-api-reference/deckgl-google-maps/google-maps-overlay?section=constructor)

## Goal
Create a new `HexagonLayer` to show the expensive areas

```javascript
const hexagon = () => new HexagonLayer({
  id: 'hex',
  data: sourceData,
  getPosition: d => [d.longitude, d.latitude],
  getElevationWeight: d => (d.pris * 2),
  elevationScale: 2,
  extruded: true,
  radius: 150,
  opacity: 0.6,
  coverage: 0.88,
  lowerPercentile: 50
});
```

```html
<span class="button" id="heatmap" onClick="setHeatMap()">Dyraste område</span>
```

This is an example of creating the scatterplot layer for representing each toilet.

Can you create a new layer to show the hexagon layer?

## Hint
Example of the scatterplot layer implementation
```javascript
window.setPriceOverview = () => {
  overlay.setProps({
    layers: [
        scatterplot()
    ],
  });
}
```
