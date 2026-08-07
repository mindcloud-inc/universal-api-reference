# Get Events with BlackBaud

## Endpoint

- **Method:** `GET`
- **Path:** `event/v1/eventlist`
- **Base URL:** `https://api.sky.blackbaud.com/`
- **Official documentation:** [Get Events](https://developer.blackbaud.com/skyapi/products/altru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter events by name when supported by the endpoint. |
| `limit` | query | `number` | no | Maximum number of events to return. |
| `offset` | query | `number` | no | Number of rows to skip before returning events. |
