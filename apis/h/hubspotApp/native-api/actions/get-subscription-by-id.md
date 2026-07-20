# Get Subscription by ID with HubSpot

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/subscriptions/:subscriptionId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Subscription by ID](https://developers.hubspot.com/docs/api-reference/latest/crm/objects/commerce-subscriptions/get-commerce-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | The unique ID of the subscription to retrieve. |
| `properties[]` | query | `array<string>` | no | Subscription properties to return in the response. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Subscription properties to return with value history. |
| `associations` | query | `string` | no | Associated object types to include as associated IDs. |
| `archived` | query | `boolean` | no | Whether to return archived subscription records. |
| `idProperty` | query | `string` | no | The unique property to use for subscriptionId instead of the default record ID. |
