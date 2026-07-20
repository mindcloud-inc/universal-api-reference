# Get IP Selected Fields with ipdata.co

## Endpoint

- **Method:** `GET`
- **Path:** `/:ip`
- **Base URL:** `https://api.ipdata.co`
- **Official documentation:** [Get IP Selected Fields](https://docs.ipdata.co/docs/filtering-response-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | no | The IP address to look up. |
| `fields` | query | `string` | yes | Comma-separated response fields to return. |
