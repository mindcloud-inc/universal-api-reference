# Retrieve Inbound Campaign Messages with boomApp Connect

Retrieves inbound campaign messages from boomApp Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/get-inbound`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Retrieve Inbound Campaign Messages](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after_ref` | query | `number` | no | Return inbound messages on or after this inbound reference. |
| `from` | query | `string` | no | Filter by sender number. |
| `after` | query | `string` | no | Return inbound messages on or after this datetime. |
| `before` | query | `string` | no | Return inbound messages on or before this datetime. |
| `to_inbound_number` | query | `number` | no | Filter by inbound campaign number. |
| `per_page` | query | `number` | no | Number of inbound messages per page. |
