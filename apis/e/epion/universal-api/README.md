# <img src="https://images.mindcloud.co/apps/icons/epion_1776432274462.png" alt="Epion logo" width="28" height="28"> Epion: Universal API

Access current Epion Air indoor air-quality measurements, including CO2, temperature, humidity, and pressure readings for devices connected to an Epion account.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/epion/latest
- **Category:** IT Operations / Observability
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://epion.nl
- **Vendor API docs:** https://epion.nl/integraties

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Current Measurements](actions/list-current-measurements.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/epion/latest/actions/list-current-measurements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [List Current Measurements](actions/list-current-measurements.md) | GET | Retrieves current device measurements from Epion. |

