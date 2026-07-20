# List parcel transactions with Zillow Public Records

Retrieves parcel transactions from Zillow Public Records by parcel ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/pub/parcels/:parcelId/transactions`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [List parcel transactions](https://www.zillowgroup.com/developers/api/public-data/public-records-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parcelId` | path | `string` | yes | Bridge parcel identifier used to fetch transaction history for a parcel. |
