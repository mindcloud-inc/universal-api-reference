# List States by Country with turboSMTP

Retrieves states for a country from turboSMTP.

## Endpoint

- **Method:** `GET`
- **Path:** `/meta/state/{isoCode}`
- **Base URL:** `https://pro.api.serversmtp.com/api/v2`
- **Official documentation:** [List States by Country](https://serversmtp.com/turbo-api/#/meta/getStatesByCountry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isoCode` | path | `string` | yes | Two-letter country ISO code. |
