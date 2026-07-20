# Get Webserver Status with Airzone Cloud

Retrieves webserver status and config from Airzone Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/ws/{wsId}/status`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Get Webserver Status](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devices` | query | `string` | no | Optional flag. Set to `1` to include device data when the authenticated user is an installation admin. |
| `installation_id` | query | `string` | yes | The installation ID that owns the webserver. |
| `wsId` | path | `string` | yes | The Airzone webserver identifier. |
