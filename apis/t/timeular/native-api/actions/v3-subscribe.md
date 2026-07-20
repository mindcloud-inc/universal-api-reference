# V3 Subscribe with Timeular

Creates a new webhook subscription in the Timeular v3 API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/webhooks/subscription`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Subscribe](https://developers.early.app/#f3ed186d-288f-4a7e-9a35-31c849f936c2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event` | body | `string` | yes |
| `target_url` | body | `string` | no |
