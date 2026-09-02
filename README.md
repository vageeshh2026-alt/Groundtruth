## 🗺️ Groundtruth

**Routes that account for what's actually happening — not just distance.**

Groundtruth is a route-planning demo that layers live weather, crowdsourced hazard reports, and traffic conditions on top of standard routing, then recommends the route with the lowest real-world risk — not just the shortest one.

### Features

- **Condition-aware routing** — pulls multiple route alternatives and re-scores them using live weather and nearby hazard reports, not just raw travel time
- **Live weather overlay** — checks conditions along each route (rain, wind) via Open-Meteo and factors them into a risk score
- **Crowdsourced hazard reporting** — tap the map to report accidents, potholes, flooding, or heavy traffic; reports are shared with everyone using the app, Waze-style
- **Live GPS tracking** — shows your real-time position and accuracy on the map
- **Risk breakdown panel** — see weather, traffic, and road conditions for the selected route at a glance, with a Low/Moderate/High risk badge

### How it works

- **Roads & routing:** [OpenStreetMap](https://www.openstreetmap.org/) + the open-source [OSRM](http://project-osrm.org/) engine
- **Geocoding:** [Nominatim](https://nominatim.org/)
- **Weather:** [Open-Meteo](https://open-meteo.com/)
- **Map rendering:** [Leaflet](https://leafletjs.com/)
- **Hazard reports:** stored and shared across all users of the demo

Each route's estimated time is adjusted by a penalty for detected rain, strong wind, and nearby hazard reports, then routes are ranked so the lowest-risk option is recommended by default — even if it's not the fastest one.

> Scoring weights are illustrative for this MVP; a production version would tune them against real incident and delay data.

### Tech Stack

`JavaScript` `Leaflet.js` `OSRM` `Open-Meteo API` `Nominatim`
