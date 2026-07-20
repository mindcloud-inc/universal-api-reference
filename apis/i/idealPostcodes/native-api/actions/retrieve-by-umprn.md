# Retrieve by UMPRN with Ideal Postcodes

Retrieves a multiple occupancy address from Ideal Postcodes by UMPRN.

## Endpoint

- **Method:** `GET`
- **Path:** `/umprn/:umprn`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Retrieve by UMPRN](https://docs.ideal-postcodes.co.uk/docs/api/umprn)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `umprn` | path | `number` | yes | Multiple Residence Unique ID to retrieve. |
| `filter` | query | `string` | no | Comma-separated whitelist of address fields to return. |
