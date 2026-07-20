# Link Location to Offer with Fidel API

Links a location to an offer in Fidel API.

## Endpoint

- **Method:** `POST`
- **Path:** `/offers/:offerId/locations/:locationId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Link Location to Offer](https://reference.fidel.uk/reference/link-location-to-offer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offerId` | path | `string` | yes | — |
| `locationId` | path | `string` | yes | Id of the location. |
