# Recon Report with Walmart

Retrieves details of all orders with optional search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/report/reconreport/reconFileJson`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Recon Report](https://developer.walmart.com/global-marketplace/reference/getallorders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `reportDate` | query | `string` | yes |
