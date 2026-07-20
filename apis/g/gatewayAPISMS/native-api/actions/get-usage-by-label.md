# Get Usage by Label with GatewayAPI SMS

Retrieves GatewayAPI SMS usage by label and country.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/usage/labels`
- **Base URL:** `https://gatewayapi.com`
- **Official documentation:** [Get Usage by Label](https://gatewayapi.com/docs/apis/statistics/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Start date in YYYY-MM-DD format. |
| `to` | body | `string` | yes | End date in YYYY-MM-DD format. |
| `label` | body | `string` | no | Optional message label to filter on. |
