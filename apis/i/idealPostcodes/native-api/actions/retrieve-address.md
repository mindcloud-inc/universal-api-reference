# Retrieve Address with Ideal Postcodes

Retrieves a US address from Ideal Postcodes by address ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete/addresses/:address/usa`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Retrieve Address](https://docs.ideal-postcodes.co.uk/docs/api/retrieve-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Address suggestion ID to retrieve in US format. |
| `tags` | query | `string` | no | Comma-separated tags to associate with the retrieval request. |
