# Where the ISS at: Native API Reference

A consolidated summary of Where the ISS at's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://wheretheiss.at/w/developer
- **API base URL:** `https://api.wheretheiss.at/v1`

## Authentication

### No authentication

This API does not require request authentication.

[Official authentication documentation](https://wheretheiss.at/w/developer)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Coordinate Timezone](actions/get-coordinate-timezone.md) | `GET /coordinates/:latitude,:longitude` | [docs](https://wheretheiss.at/w/developer) |
| [Get Satellite Position](actions/get-satellite-position.md) | `GET /satellites/:satelliteId` | [docs](https://wheretheiss.at/w/developer) |
| [Get Satellite Positions](actions/get-satellite-positions.md) | `GET /satellites/:satelliteId/positions` | [docs](https://wheretheiss.at/w/developer) |
| [Get Satellite TLE](actions/get-satellite-tle.md) | `GET /satellites/:satelliteId/tles` | [docs](https://wheretheiss.at/w/developer) |
| [List Satellites](actions/list-satellites.md) | `GET /satellites` | [docs](https://wheretheiss.at/w/developer) |
