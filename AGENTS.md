# Map dependencies

- CARTO tiles require `cartoBasemapsApiKey` in `config.js`. Error tiles may return HTTP 200 and fire image load events, so verify tile contents visually, not just network status. This browser-visible key should be restricted to the site's domains in the CARTO dashboard.

- Leaflet 1.9.4 is vendored in `assets/vendor/leaflet` so map startup does not depend on an external script CDN. Keep its license and image assets, and update the integrity hashes in `index.html` if replacing the library. A wrong integrity hash causes browsers to reject the resource.
