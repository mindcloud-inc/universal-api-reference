# Update Collection with Qlik

Updates an existing collection in Qlik.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/collections/:collectionId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Update Collection](https://qlik.dev/apis/rest/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Qlik collection ID. |
| `name` | body | `string` | no | Collection name. |
| `description` | body | `string` | no | Collection description. |
