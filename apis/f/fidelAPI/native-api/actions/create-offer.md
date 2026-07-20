# Create Offer with Fidel API

Creates a new offer in Fidel API.

## Endpoint

- **Method:** `POST`
- **Path:** `/offers`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Create Offer](https://reference.fidel.uk/reference/create-offer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brandId` | body | `string` | yes | — |
| `countryCode` | body | `string` | yes | ISO 3166-1 alpha-3 country code where the offer is active. |
| `name` | body | `string` | yes | Name of the offer. |
| `startDate` | body | `string` | yes | Offer start date in YYYY-MM-DDThh:mm:ss format. |
| `type.name` | body | `string` | yes | Offer type name. |
| `type.value` | body | `number` | yes | Offer type value. |
