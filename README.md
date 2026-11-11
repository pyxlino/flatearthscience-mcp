# Flat Earth Science MCP app

Run Flat Earth Science's calculators and read its tested claims.

Ask how much of a lighthouse the curve of the Earth hides, how far the horizon is, how far apart two cities are on a flat Earth map, where the Sun is at a given time and place, or how big Greenland really is. The answers come from the same calculations as flatearthscience.org.

- Website: https://flatearthscience.org
- Documentation: https://flatearthscience.org/app
- Privacy: https://flatearthscience.org/privacy
- Terms: https://flatearthscience.org/terms

This repository documents the hosted connector. It does not contain the
website or its code.

## Connect

- Endpoint: `https://flatearthscience.org/api/mcp`
- Transport: Streamable HTTP
- Authentication: none (no account, sign-in or API key)

```json
{ "mcpServers": { "flat-earth-science": { "url": "https://flatearthscience.org/api/mcp" } } }
```

In ChatGPT, add it as a custom MCP server with no authentication. In
Claude, open Customize, then Connectors, choose Add custom connector and enter the URL.

## Tools

All tools are read-only.

| Tool | What it does |
|---|---|
| `calculate_curvature` | Calculates how much of a distant target the Earth's curvature hides, from the surface distance, the observer's eye height, the target's height and an assumed refraction coefficient. |
| `get_horizon_distance` | Gives the distance to the horizon from an eye height above a smooth sphere, and how far a taller object such as a mast stays in straight sight. |
| `compare_flat_map_distance` | Compares the distance between two cities on a north-polar flat-Earth map with their great-circle distance over a sphere. |
| `get_flight_distance` | Calculates the great-circle distance between two places in kilometres, miles and nautical miles, with the initial and final compass bearings. |
| `get_sun_position` | Calculates the Sun's altitude and compass bearing at a place, date and UTC time, with the shadow of a 1 m upright and the day's sunrise and sunset in UTC. A place is one of the website's 20 cities or a latitude and longitude; without a date and time the result is for the current moment. |
| `get_daylight_hours` | Calculates the length of daylight at a place on a date, with sunrise and sunset in UTC, for the UTC day from midnight to midnight. |
| `compare_true_size` | Shows how much a Mercator map distorts a country's area, from its real area and the latitude it is drawn at. |
| `find_claims` | Searches the website's tested claims and flat-earth investigations, or returns one by id. |

## Try asking

- "How much of a 10 m lighthouse is hidden by the curve of the Earth over 20 km, seen from 2 m?"
- "How far apart are Sydney and Santiago on the flat Earth map compared with the real distance?"
- "What is the verdict on the Bermuda Triangle?"

## Report an issue

Open an issue in this repository or email support@flatearthscience.org.

## License

The documentation files in this repository are MIT licensed (see
[LICENSE](LICENSE)). The Flat Earth Science website, its content, data and brand are
not covered by this license.
