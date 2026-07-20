# List Customer Infos with ThingsBoard

Retrieves customer info records from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/customerInfos/all`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [List Customer Infos](https://thingsboard.cloud/swagger-ui/index.html#/customer-controller/getAllCustomerInfos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | yes | Maximum number of customer info records to return in one page. |
| `page` | query | `number` | yes | Zero-based page number. |
