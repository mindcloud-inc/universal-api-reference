# Get Parcel with EasyPost

Retrieves details for a parcel from EasyPost.

## Endpoint

- **Method:** `GET`
- **Path:** `/parcels/:id`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Get Parcel](https://docs.easypost.com/docs/parcels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Parcel ID, beginning with prcl_. |
