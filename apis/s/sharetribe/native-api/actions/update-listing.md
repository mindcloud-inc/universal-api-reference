# Update Listing with Sharetribe

Updates an existing listing in Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `listings/update`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Update Listing](https://www.sharetribe.com/api-reference/integration.html#update-listing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the listing that is being updated. |
| `title` | body | `string` | no | Listing title. |
| `description` | body | `string` | no | Listing description. |
| `geolocation` | body | `object` | no | Listing latitude and longitude object. Pass null to remove. |
| `price` | body | `object` | no | Listing money object with amount and currency. Pass null to remove. |
| `availabilityPlan` | body | `object` | no | Full listing availability plan object. Pass null to reset to default daily availability. |
| `publicData` | body | `object` | no | Listing public extended data object. |
| `privateData` | body | `object` | no | Listing private extended data object. |
| `metadata` | body | `object` | no | Listing public metadata object. |
| `images[]` | body | `array<string>` | no | Ordered list of uploaded image IDs for the listing. |
