# List Member Activities with Easymailing

Retrieves member activities from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/members/{{memberUuid}}/activities`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [List Member Activities](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `memberUuid` | path | `string` | yes | Member UUID. |
