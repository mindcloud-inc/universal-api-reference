# Get Condition Field with Easymailing

Retrieves a condition field from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/condition_fields/{{uuid}}`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Condition Field](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `uuid` | path | `string` | yes | Condition field UUID. |
