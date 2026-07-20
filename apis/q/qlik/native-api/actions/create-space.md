# Create Space with Qlik

Creates a new space in your Qlik tenant.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/spaces`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Create Space](https://qlik.dev/apis/rest/spaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Space name. |
| `type` | body | `string` | yes | Space type. |
| `description` | body | `string` | no | Space description. |
