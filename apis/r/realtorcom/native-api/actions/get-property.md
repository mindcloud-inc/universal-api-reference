# Get Property with Realtor.com

## Endpoint

- **Method:** `GET`
- **Path:** `/odata/Property('{{listingKey}}')`
- **Base URL:** `https://api.listhub.com`
- **Official documentation:** [Get Property](https://www.listhub.com/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listingKey` | path | `string` | yes | Unique ListHub ListingKey, for example 3yd-FAKE-1. |
| `$select` | query | `string` | no | Comma-separated RESO field names to return for the listing. |
