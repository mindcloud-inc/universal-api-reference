# Get Group with Easymailing

Retrieves a group from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/groups/{{uuid}}`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Group](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `uuid` | path | `string` | yes | Group UUID. |
