# List Subscriptions with HubSpot

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/subscriptions`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Subscriptions](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/commerce-subscriptions/get-commerce-subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no | Subscription properties to return in the response. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Subscription properties to return with value history. |
| `associations` | query | `string` | no | Associated object types to include as associated IDs. |
| `archived` | query | `boolean` | no | Whether to return archived subscription records. |
