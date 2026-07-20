# Get Availability with Channex

Retrieves room type availability from Channex.

## Endpoint

- **Method:** `GET`
- **Path:** `/availability`
- **Base URL:** `https://staging.channex.io/api/v1`
- **Official documentation:** [Get Availability](https://docs.channex.io/api-v.1-documentation/ari#get-availability-per-room-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[property_id]` | query | `string` | yes | Property UUID used to scope the availability query. |
| `filter[date][gte]` | query | `date` | yes | Start date in YYYY-MM-DD format. |
| `filter[date][lte]` | query | `date` | yes | End date in YYYY-MM-DD format. |
