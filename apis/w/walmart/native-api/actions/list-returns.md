# List Returns with Walmart

Retrieve details for return orders that match the filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/returns`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Returns](https://developer.walmart.com/us-marketplace/reference/getreturns#:~:text=Utilities-,Returns,-GET)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | — |
| `returnType` | query | `list<string>` | no | — |
| `returnOrderId` | query | `string` | no | — |
| `customerOrderId` | query | `string` | no | — |
| `returnCreationStartDate` | query | `date` | no | — |
| `returnCreationEndDate` | query | `date` | no | — |
| `returnLastModifiedStartDate` | query | `date` | no | — |
| `returnLastModifiedEndDate` | query | `date` | no | — |
| `replacementInfo` | query | `boolean` | no | Format: `toggle`. |
| `dynamicSandbox` | query | `boolean` | no | — |
