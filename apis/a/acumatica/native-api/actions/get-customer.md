# Get Customer with Acumatica

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Customer/:id`
- **Base URL:** `{uRL}`
- **Official documentation:** [Get Customer](https://beacon.acumatica.com/r/Integration-Development-Guide/REST-API-Examples/Basic-Requests/Retrieve-a-Record-by-ID)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Acumatica entity ID (GUID) returned in the record's id field. |
| `$select` | query | `string` | no | Comma-separated entity fields to return. |
| `$expand` | query | `string` | no | Comma-separated detail or linked entities to expand. |
| `$custom` | query | `string` | no | Comma-separated custom fields to return. |
