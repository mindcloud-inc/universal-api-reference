# List Payment Links with Payfunnels

Retrieves a list of payment links from Payfunnels.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/paymentlinks`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [List Payment Links](https://api.payfunnels.com/api/docs/#returns-list-of-payment-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Filter payment links by type. |
