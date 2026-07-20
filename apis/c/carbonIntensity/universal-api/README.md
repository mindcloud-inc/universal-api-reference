# <img src="https://images.mindcloud.co/apps/icons/157384_1781291789417.png" alt="Carbon Intensity logo" width="28" height="28"> Carbon Intensity: Universal API

Public UK National Energy System Operator carbon intensity and generation mix data for national and regional forecasting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/carbonIntensity/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://api.carbonintensity.org.uk/
- **Vendor API docs:** https://api.carbonintensity.org.uk/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Carbon Intensity](actions/get-current-carbon-intensity.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/carbonIntensity/latest/actions/get-current-carbon-intensity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Carbon Intensity

| Action | Method | Description |
| --- | --- | --- |
| [Get Carbon Intensity Between Times](actions/get-carbon-intensity-between-times.md) | GET | Retrieves carbon intensity between two specified datetimes. |
| [Get Carbon Intensity By Date](actions/get-carbon-intensity-by-date.md) | GET | Retrieves carbon intensity for a specific date. |
| [Get Carbon Intensity By Date and Settlement Period](actions/get-carbon-intensity-by-date-and-settlement-period.md) | GET | Retrieves carbon intensity for a date and settlement period. |
| [Get Carbon Intensity Factors](actions/get-carbon-intensity-factors.md) | GET | Retrieves carbon intensity factors for fuel types. |
| [Get Carbon Intensity Forward 24 Hours](actions/get-carbon-intensity-forward24-hours.md) | GET | Retrieves carbon intensity for 24 hours after a datetime. |
| [Get Carbon Intensity Forward 48 Hours](actions/get-carbon-intensity-forward48-hours.md) | GET | Retrieves carbon intensity for 48 hours after a datetime. |
| [Get Carbon Intensity From Time](actions/get-carbon-intensity-from-time.md) | GET | Retrieves carbon intensity from a specific datetime. |
| [Get Carbon Intensity Previous 24 Hours](actions/get-carbon-intensity-previous24-hours.md) | GET | Retrieves carbon intensity for 24 hours before a datetime. |
| [Get Carbon Intensity Statistics](actions/get-carbon-intensity-statistics.md) | GET | Retrieves carbon intensity statistics between two specified datetimes. |
| [Get Carbon Intensity Statistics By Block](actions/get-carbon-intensity-statistics-by-block.md) | GET | Retrieves block-based carbon intensity statistics between two datetimes. |
| [Get Current Carbon Intensity](actions/get-current-carbon-intensity.md) | GET | Retrieves current carbon intensity for Great Britain. |
| [Get Today Carbon Intensity](actions/get-today-carbon-intensity.md) | GET | Retrieves today's carbon intensity for Great Britain. |

### Generation Mix

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Generation Mix](actions/get-current-generation-mix.md) | GET | Retrieves the current generation mix for Great Britain. |
| [Get Generation Mix Between Times](actions/get-generation-mix-between-times.md) | GET | Retrieves generation mix between two specified datetimes. |
| [Get Generation Mix Previous 24 Hours](actions/get-generation-mix-previous24-hours.md) | GET | Retrieves generation mix for 24 hours before a datetime. |

### Regional Carbon Intensity

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Regional Carbon Intensity](actions/get-current-regional-carbon-intensity.md) | GET | Retrieves current carbon intensity for Great Britain regions. |
| [Get Regional Carbon Intensity Between Times](actions/get-regional-carbon-intensity-between-times.md) | GET | Retrieves regional carbon intensity between two specified datetimes. |
| [Get Regional Carbon Intensity Between Times By Postcode](actions/get-regional-carbon-intensity-between-times-by-postcode.md) | GET | Retrieves regional carbon intensity between datetimes by postcode. |
| [Get Regional Carbon Intensity Between Times By Region ID](actions/get-regional-carbon-intensity-between-times-by-region-id.md) | GET | Retrieves regional carbon intensity between datetimes by region. |
| [Get Regional Carbon Intensity By Postcode](actions/get-regional-carbon-intensity-by-postcode.md) | GET | Retrieves current regional carbon intensity for a postcode. |
| [Get Regional Carbon Intensity By Region ID](actions/get-regional-carbon-intensity-by-region-id.md) | GET | Retrieves current regional carbon intensity for a region. |
| [Get Regional Carbon Intensity Forward 24 Hours](actions/get-regional-carbon-intensity-forward24-hours.md) | GET | Retrieves 24-hour regional carbon intensity after a datetime. |
| [Get Regional Carbon Intensity Forward 24 Hours By Postcode](actions/get-regional-carbon-intensity-forward24-hours-by-postcode.md) | GET | Retrieves 24-hour regional carbon intensity after a datetime by postcode. |
| [Get Regional Carbon Intensity Forward 24 Hours By Region ID](actions/get-regional-carbon-intensity-forward24-hours-by-region-id.md) | GET | Retrieves 24-hour regional carbon intensity after a datetime by region. |
| [Get Regional Carbon Intensity Forward 48 Hours](actions/get-regional-carbon-intensity-forward48-hours.md) | GET | Retrieves 48-hour regional carbon intensity after a datetime. |
| [Get Regional Carbon Intensity Forward 48 Hours By Postcode](actions/get-regional-carbon-intensity-forward48-hours-by-postcode.md) | GET | Retrieves 48-hour regional carbon intensity after a datetime by postcode. |
| [Get Regional Carbon Intensity Forward 48 Hours By Region ID](actions/get-regional-carbon-intensity-forward48-hours-by-region-id.md) | GET | Retrieves 48-hour regional carbon intensity after a datetime by region. |
| [Get Regional Carbon Intensity Previous 24 Hours](actions/get-regional-carbon-intensity-previous24-hours.md) | GET | Retrieves 24-hour regional carbon intensity before a datetime. |
| [Get Regional Carbon Intensity Previous 24 Hours By Postcode](actions/get-regional-carbon-intensity-previous24-hours-by-postcode.md) | GET | Retrieves 24-hour regional carbon intensity before a datetime by postcode. |
| [Get Regional Carbon Intensity Previous 24 Hours By Region ID](actions/get-regional-carbon-intensity-previous24-hours-by-region-id.md) | GET | Retrieves 24-hour regional carbon intensity before a datetime by region. |

