# Retrieve by UDPRN with Ideal Postcodes

Retrieves an address from Ideal Postcodes by UDPRN.

## Endpoint

- **Method:** `GET`
- **Path:** `/udprn/:udprn`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Retrieve by UDPRN](https://docs.ideal-postcodes.co.uk/docs/api/udprn)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `udprn` | path | `string` | yes | Unique Delivery Point Reference Number to retrieve. |
| `filter` | query | `string` | no | Comma-separated whitelist of address fields to return. |
