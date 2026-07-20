# Get Meeting with Avoma

Retrieves a meeting from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meetings/:uuid/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Get Meeting](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Unique ID of the meeting. |
| `include_crm_associations` | query | `boolean` | no | Whether to include CRM associations in the response. |
