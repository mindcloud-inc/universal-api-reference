# Resolve Address with Ideal Postcodes

Retrieves a UK address from Ideal Postcodes by address ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete/addresses/:address/gbr`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Resolve Address](https://docs.ideal-postcodes.co.uk/docs/api/resolve-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Address suggestion ID to resolve in UK format. |
| `tags` | query | `string` | no | Comma-separated tags to associate with the resolution request. |
