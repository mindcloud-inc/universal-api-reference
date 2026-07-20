# Get Market Status with Finage

Retrieves market status from Finage.

## Endpoint

- **Method:** `GET`
- **Path:** `/marketstatus`
- **Base URL:** `https://api.finage.co.uk`
- **Official documentation:** [Get Market Status](https://finage.co.uk/docs/api/fundamentals/market-status-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Country code to check market status for. |
| `currencies` | query | `boolean` | no | Include forex and crypto market status in the response. |
| `holidays` | query | `boolean` | no | Include market holidays for the selected country. |
| `trading_hours` | query | `boolean` | no | Include regular trading hours in the response. |
| `extended_hours` | query | `boolean` | no | Include extended-hours status in the response. |
