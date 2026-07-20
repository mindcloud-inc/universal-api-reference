# Cleanse Address with Ideal Postcodes

Finds the closest matching address in Ideal Postcodes.

## Endpoint

- **Method:** `POST`
- **Path:** `/cleanse/addresses`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Cleanse Address](https://docs.ideal-postcodes.co.uk/docs/api/address-cleanse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Freeform address input to cleanse. |
| `postcode` | body | `string` | no | Optional postcode for the address. |
| `post_town` | body | `string` | no | Optional town or city component for the address. |
| `county` | body | `string` | no | Optional county or state component for the address. |
| `context` | query | `string` | no | Country context to use when cleansing the address, for example GBR. |
| `tags` | query | `string` | no | Comma-separated tags used to annotate the request context. |
