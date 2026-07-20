# Create Listing with Sharetribe

Creates a new listing in Sharetribe.

## Endpoint

- **Method:** `POST`
- **Path:** `listings/create`
- **Base URL:** `https://flex-integ-api.sharetribe.com/v1/integration_api`
- **Official documentation:** [Create Listing](https://www.sharetribe.com/api-reference/integration.html#create-listing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Listing title. |
| `authorId` | body | `string` | yes | The ID of the marketplace user to whom the listing belongs. |
| `state` | body | `string` | yes | Initial listing state: published or pendingApproval. |
| `description` | body | `string` | no | Listing description. |
| `geolocation` | body | `object` | no | Listing latitude and longitude object. |
| `price` | body | `object` | no | Listing money object with amount and currency. |
| `availabilityPlan` | body | `object` | no | Listing availability plan object. |
| `publicData` | body | `object` | no | Listing public extended data object. |
| `privateData` | body | `object` | no | Listing private extended data object. |
| `metadata` | body | `object` | no | Listing public metadata object. |
| `images[]` | body | `array<string>` | no | Ordered list of uploaded image IDs for the listing. |
