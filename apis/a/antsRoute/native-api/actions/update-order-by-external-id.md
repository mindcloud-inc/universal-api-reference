# Update Order by External ID with AntsRoute

Updates an existing order in AntsRoute by external ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/capi/order/external-id/:externalId`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Update Order by External ID](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/patchOrderByExternalId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comments` | body | `string` | no | Order comments. |
| `externalId` | path | `string` | yes | External order ID. |
