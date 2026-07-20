# Get Customer by ID with AntsRoute

Retrieves a customer from AntsRoute by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/customer/id/:id`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Get Customer by ID](https://app.antsroute.com/doc-api/index.html#/Customer/getCustomerById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `includeSectors` | query | `boolean` | no | Return sectors assigned to this customer |
