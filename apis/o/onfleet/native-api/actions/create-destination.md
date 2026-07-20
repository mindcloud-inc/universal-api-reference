# Create Destination with Onfleet

Creates a new destination in Onfleet.

## Endpoint

- **Method:** `POST`
- **Path:** `/destinations`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Create Destination](https://docs.onfleet.com/reference/create-destination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address.number` | body | `string` | yes | The number component of the destination address. |
| `address.street` | body | `string` | yes | The street component of the destination address. |
| `address.city` | body | `string` | yes | The city component of the destination address. |
| `address.country` | body | `string` | yes | The country component of the destination address. |
| `address.name` | body | `string` | no | Optional name associated with this address. |
| `address.apartment` | body | `string` | no | Optional apartment or suite information. |
| `address.state` | body | `string` | no | Optional state or province information. |
| `address.postalCode` | body | `string` | no | Optional postal or zip code. |
| `address.unparsed` | body | `string` | no | Optional complete address string to geocode. |
| `notes` | body | `string` | no | Optional notes about the destination. |
