# Create Collection with Qlik

Creates a new collection in Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/collections`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Create Collection](https://qlik.dev/apis/rest/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Collection name. |
| `type` | body | `string` | yes | Collection type. |
| `description` | body | `string` | no | Collection description. |
