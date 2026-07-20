# Get Subscription Form with Easymailing

Retrieves a subscription form from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/suscription_forms/{{uuid}}`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Subscription Form](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `uuid` | path | `string` | yes | Form UUID. |
