# List Processed Payments with Pinch Payments

Retrieves processed payments from Pinch Payments.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments/processed`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [List Processed Payments](https://docs.getpinch.com.au/reference/list-processed-payments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `endDate` | query | `date` | no |
| `filter` | query | `string` | no |
| `startDate` | query | `date` | no |
