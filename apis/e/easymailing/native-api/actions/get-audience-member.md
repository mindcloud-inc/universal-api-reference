# Get Audience Member with Easymailing

Retrieves an audience member from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/members/{{uuid}}`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Audience Member](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `uuid` | path | `string` | yes | Member UUID. |
