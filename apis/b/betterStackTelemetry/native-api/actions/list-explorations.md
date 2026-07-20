# List Explorations with Better Stack Telemetry

Retrieves explorations from Better Stack Telemetry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/explorations`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [List Explorations](https://betterstack.com/docs/logs/api/explorations/list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `per_page` | query | `number` | no | Number of explorations to return per page. |
| `query` | query | `string` | no | Filter explorations by search query. |
