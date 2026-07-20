# Get Customer by External ID with AntsRoute

Retrieves a customer from AntsRoute by external ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/customer/external-id/:externalId`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Get Customer by External ID](https://app.antsroute.com/doc-api/index.html#/Customer/getCustomerByExternalId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | — |
| `includeSectors` | query | `boolean` | no | Return sectors assigned to this customer |
