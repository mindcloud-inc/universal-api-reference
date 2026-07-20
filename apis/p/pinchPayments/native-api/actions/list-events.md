# List Events with Pinch Payments

Retrieves events from Pinch Payments.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [List Events](https://docs.getpinch.com.au/reference/list-all-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `endDate` | query | `date` | no |
| `eventType` | query | `string` | no |
| `startDate` | query | `date` | no |
