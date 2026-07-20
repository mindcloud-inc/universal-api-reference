# Get Collection with Qlik

Retrieves a collection from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/collections/:collectionId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get Collection](https://qlik.dev/apis/rest/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Qlik collection ID. |
