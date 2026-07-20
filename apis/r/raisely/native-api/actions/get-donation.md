# Get Donation with Raisely

Retrieves a donation from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/donations/:uuid`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Get Donation](https://developers.raisely.com/reference/getdonation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | The `uuid` of the record |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
