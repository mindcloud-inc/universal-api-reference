# List Payers with Pinch Payments

Retrieves payers from Pinch Payments.

## Endpoint

- **Method:** `GET`
- **Path:** `/payers`
- **Base URL:** `https://api.getpinch.com.au/live`
- **Official documentation:** [List Payers](https://docs.getpinch.com.au/reference/list-payers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Optional string filter to search for payers by name or email address. |
