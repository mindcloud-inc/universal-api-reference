# Get listing with Bridge Interactive Platform

Retrieves a listing from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/listings/:listingId`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get listing](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
| `listingId` | path | `string` | yes | Bridge listing identifier from the REST listings feed. |
