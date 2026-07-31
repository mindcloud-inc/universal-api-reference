# <img src="https://images.mindcloud.co/apps/icons/where-the-issat_1785420726068.png" alt="Where the ISS at logo" width="28" height="28"> Where the ISS at: Universal API

Track the International Space Station, retrieve historical orbital positions and TLE data, and look up timezone information for coordinates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whereTheISSAt/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wheretheiss.at/
- **Vendor API docs:** https://wheretheiss.at/w/developer

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Coordinate Timezone](actions/get-coordinate-timezone.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whereTheISSAt/latest/actions/get-coordinate-timezone?connectionId=$CONNECTION_ID&latitude=1&longitude=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Coordinate Timezone

| Action | Method | Description |
| --- | --- | --- |
| [Get Coordinate Timezone](actions/get-coordinate-timezone.md) | GET |  |

### Satellite

| Action | Method | Description |
| --- | --- | --- |
| [List Satellites](actions/list-satellites.md) | GET |  |

### Satellite Position

| Action | Method | Description |
| --- | --- | --- |
| [Get Satellite Position](actions/get-satellite-position.md) | GET |  |
| [Get Satellite Positions](actions/get-satellite-positions.md) | GET |  |

### Satellite Tle

| Action | Method | Description |
| --- | --- | --- |
| [Get Satellite TLE](actions/get-satellite-tle.md) | GET |  |

