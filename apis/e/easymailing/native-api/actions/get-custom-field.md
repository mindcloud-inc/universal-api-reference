# Get Custom Field with Easymailing

Retrieves a custom field from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/list_fields/{{uuid}}`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Custom Field](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `uuid` | path | `string` | yes | Custom field UUID. |
