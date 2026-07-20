# Update Order by ID with AntsRoute

Updates an existing order in AntsRoute by ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/capi/order/id/:id`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Update Order by ID](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/patchOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comments` | body | `string` | no | Order comments. |
| `id` | path | `number` | yes | Order ID. |
| `externalId` | body | `string` | no | — |
