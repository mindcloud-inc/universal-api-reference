# Get Profile with Raisely

Retrieves a profile from Raisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:path`
- **Base URL:** `https://api.raisely.com/v3`
- **Official documentation:** [Get Profile](https://developers.raisely.com/reference/getprofile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | yes | The `uuid` or `path` of the record |
| `campaign` | query | `string` | no | The `uuid`, `path` or domain of the campaign to associate with the request |
| `private` | query | `boolean` | no | Returns the full record when authenticated |
