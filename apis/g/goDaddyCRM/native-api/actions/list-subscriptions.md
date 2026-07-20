# List Subscriptions with GoDaddy CRM

Retrieves subscriptions from your GoDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/subscriptions`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [List Subscriptions](https://developer.godaddy.com/doc/endpoint/subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productGroupKeys[]` | query | `array<string>` | no | Only return subscriptions with the specified product groups. |
| `includes[]` | query | `array<string>` | no | Optional details to include in the response. |
