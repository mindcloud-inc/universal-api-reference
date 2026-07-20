# Get campaign analytics with Kite Suite

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaign/analytics`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Get campaign analytics](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign` | query | `string` | yes | Campaign ID. |
| `start` | query | `string` | no | Start date (YYYY-MM-DD). Defaults to 4 weeks prior. |
| `end` | query | `string` | no | End date (YYYY-MM-DD). Defaults to the current date. |
