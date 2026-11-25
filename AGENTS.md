# Map dependencies

- Leaflet 1.9.4 is vendored in `assets/vendor/leaflet` so map startup does not depend on an external script CDN. Keep its license and image assets, and update the integrity hashes in `index.html` if replacing the library. A wrong integrity hash causes browsers to reject the resource.
