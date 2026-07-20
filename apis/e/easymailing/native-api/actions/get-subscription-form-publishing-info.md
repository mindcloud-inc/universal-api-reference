# Get Subscription Form Publishing Info with Easymailing

Retrieves subscription form publishing info from Easymailing.

## Endpoint

- **Method:** `GET`
- **Path:** `/audiences/{{audienceUuid}}/suscription_forms/{{uuid}}/publishing-info`
- **Base URL:** `https://api.easymailing.com`
- **Official documentation:** [Get Subscription Form Publishing Info](https://developers.easymailing.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audienceUuid` | path | `string` | yes | Audience UUID. |
| `uuid` | path | `string` | yes | Form UUID. |
