# Carbon Intensity: Native API Reference

A consolidated summary of Carbon Intensity's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.carbonintensity.org.uk/
- **API base URL:** `https://api.carbonintensity.org.uk`

## Authentication

### No Authentication

This public API does not require provider credentials.

This API does not require request authentication.

[Official authentication documentation](https://api.carbonintensity.org.uk/)

## API conventions

Response data is read from `data`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Carbon Intensity Between Times](actions/get-carbon-intensity-between-times.md) | `GET /intensity/:from/:to` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity By Date](actions/get-carbon-intensity-by-date.md) | `GET /intensity/date/:date` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity By Date and Settlement Period](actions/get-carbon-intensity-by-date-and-settlement-period.md) | `GET /intensity/date/:date/:period` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity Factors](actions/get-carbon-intensity-factors.md) | `GET /intensity/factors` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity Forward 24 Hours](actions/get-carbon-intensity-forward24-hours.md) | `GET /intensity/:from/fw24h` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity Forward 48 Hours](actions/get-carbon-intensity-forward48-hours.md) | `GET /intensity/:from/fw48h` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity From Time](actions/get-carbon-intensity-from-time.md) | `GET /intensity/:from` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity Previous 24 Hours](actions/get-carbon-intensity-previous24-hours.md) | `GET /intensity/:from/pt24h` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity Statistics](actions/get-carbon-intensity-statistics.md) | `GET /intensity/stats/:from/:to` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Carbon Intensity Statistics By Block](actions/get-carbon-intensity-statistics-by-block.md) | `GET /intensity/stats/:from/:to/:block` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Current Carbon Intensity](actions/get-current-carbon-intensity.md) | `GET /intensity` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Current Generation Mix](actions/get-current-generation-mix.md) | `GET /generation` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Current Regional Carbon Intensity](actions/get-current-regional-carbon-intensity.md) | `GET /regional` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Generation Mix Between Times](actions/get-generation-mix-between-times.md) | `GET /generation/:from/:to` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Generation Mix Previous 24 Hours](actions/get-generation-mix-previous24-hours.md) | `GET /generation/:from/pt24h` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Between Times](actions/get-regional-carbon-intensity-between-times.md) | `GET /regional/intensity/:from/:to` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Between Times By Postcode](actions/get-regional-carbon-intensity-between-times-by-postcode.md) | `GET /regional/intensity/:from/:to/postcode/:postcode` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Between Times By Region ID](actions/get-regional-carbon-intensity-between-times-by-region-id.md) | `GET /regional/intensity/:from/:to/regionid/:regionid` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity By Postcode](actions/get-regional-carbon-intensity-by-postcode.md) | `GET /regional/postcode/:postcode` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity By Region ID](actions/get-regional-carbon-intensity-by-region-id.md) | `GET /regional/regionid/:regionid` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Forward 24 Hours](actions/get-regional-carbon-intensity-forward24-hours.md) | `GET /regional/intensity/:from/fw24h` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Forward 24 Hours By Postcode](actions/get-regional-carbon-intensity-forward24-hours-by-postcode.md) | `GET /regional/intensity/:from/fw24h/postcode/:postcode` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Forward 24 Hours By Region ID](actions/get-regional-carbon-intensity-forward24-hours-by-region-id.md) | `GET /regional/intensity/:from/fw24h/regionid/:regionid` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Forward 48 Hours](actions/get-regional-carbon-intensity-forward48-hours.md) | `GET /regional/intensity/:from/fw48h` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Forward 48 Hours By Postcode](actions/get-regional-carbon-intensity-forward48-hours-by-postcode.md) | `GET /regional/intensity/:from/fw48h/postcode/:postcode` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Forward 48 Hours By Region ID](actions/get-regional-carbon-intensity-forward48-hours-by-region-id.md) | `GET /regional/intensity/:from/fw48h/regionid/:regionid` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Previous 24 Hours](actions/get-regional-carbon-intensity-previous24-hours.md) | `GET /regional/intensity/:from/pt24h` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Previous 24 Hours By Postcode](actions/get-regional-carbon-intensity-previous24-hours-by-postcode.md) | `GET /regional/intensity/:from/pt24h/postcode/:postcode` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Regional Carbon Intensity Previous 24 Hours By Region ID](actions/get-regional-carbon-intensity-previous24-hours-by-region-id.md) | `GET /regional/intensity/:from/pt24h/regionid/:regionid` | [docs](https://api.carbonintensity.org.uk/) |
| [Get Today Carbon Intensity](actions/get-today-carbon-intensity.md) | `GET /intensity/date` | [docs](https://api.carbonintensity.org.uk/) |
