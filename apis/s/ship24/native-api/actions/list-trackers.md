# List Trackers with Ship24

Retrieves existing shipment trackers from Ship24.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/trackers`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [List Trackers](https://docs.ship24.com/tracking-api-reference/#/operations/list-trackers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | yes | The page index, starting from 1. |
| `limit` | query | `number` | yes | The maximum number of trackers returned per page. |
| `sort` | query | `number` | no | Use 1 for oldest-first and -1 for newest-first by createdAt. Accepted values: `0`, `1`. |
