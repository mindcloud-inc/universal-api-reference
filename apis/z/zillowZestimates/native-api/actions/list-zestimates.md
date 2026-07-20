# List zestimates with Zillow Zestimates

Retrieves current property, rental, and foreclosure Zestimates from Zillow.

## Endpoint

- **Method:** `GET`
- **Path:** `/zestimates_v2/zestimates`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List zestimates](https://www.zillowgroup.com/developers/api/zestimate/zestimates-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | no | Street address to look up a Zestimate for a property. |
| `zpid.in` | query | `string` | no | Comma-separated list of Zillow property IDs to look up. Send multiple values as a string separated by `,`. |
