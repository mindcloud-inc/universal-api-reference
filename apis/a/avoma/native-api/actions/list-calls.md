# List Calls with Avoma

Retrieves calls from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/calls/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [List Calls](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Retrieve calls started at or after this UTC datetime. Use ISO 8601. |
| `to_date` | query | `string` | yes | Retrieve calls started at or before this UTC datetime. Use ISO 8601. |
| `direction` | query | `string` | no | Filter calls by direction, for example inbound or outbound. |
