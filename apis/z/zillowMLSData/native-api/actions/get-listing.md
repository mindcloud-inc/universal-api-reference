# Get listing with Zillow MLS Data

Retrieves a specific listing from Zillow MLS Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/listings/:listingId`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get listing](https://www.zillowgroup.com/developers/api/mls-broker-data/mls-listings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code that contains the listing. |
| `listingId` | path | `string` | yes | Listing identifier from the Bridge dataset. |
