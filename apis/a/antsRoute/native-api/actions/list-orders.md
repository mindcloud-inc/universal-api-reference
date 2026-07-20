# List Orders with AntsRoute

Finds orders in AntsRoute by selected criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/order`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [List Orders](https://app.antsroute.com/doc-api/index.html#/Service%2FDelivery%2FCollect/findOrder)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maxDate` | query | `date` | no | Filter by schedule date less than this date |
| `minDate` | query | `date` | no | Filter by schedule date greater than this date |
| `states[]` | query | `array<string>` | no | — |
