# OneTripTap

[![Open Site](https://img.shields.io/badge/Live-Demo-blue)](https://antonanderssonmedia.github.io/OneTripTap/)

WebXR AR visualization for placing a city map in physical space and exploring:
- bus trip events
- date-filtered event points
- road overlays

## Requirements

- Android phone with ARCore support
- Chrome with WebXR support
- HTTPS origin or localhost

## Run locally

1. Start a local server:
   - `npm start`
   - or any static server you prefer
2. Open the app in Chrome on a supported Android device.
3. Tap **Enter AR** to begin placement and interaction.

Personally I used ngrok to start an https server by running 
- "npx http-server -p 8080" first, followed by:
- "npx ngrok http 8080"
(in another terminal window)

## Project files

- `index.html` - UI and import map
- `main.js` - AR session, map placement, event and road rendering logic
- `style.css` - UI overlay styling
- `bus_data_trimmed.geojson` - bus trip/event data
- `OSMroads-nkpg-new.geojson` - road data overlay
- `viscenter-norrkoping-map.png` - map texture

## Notes

- Data and map calibration are tuned for Norrkoping.
- This project currently has no automated tests.
- It can be used on any table surface but is intended for the physical map table i.e. "digital twin" of Norrköping located at Visualization Center C

This visualization allows for: 
  - Exploration of singular trips, with expressive color coding to show speed values across each trip
  - Tap to see more information about the trip values at the interaction point
  - Toggles to show/ hide all parts except the trajectory ribbons

