# Get Profile with Google Mail

Retrieves the current user's Gmail profile.

## Endpoint

- **Method:** `GET`
- **Path:** `/profile`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Get Profile](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users/getProfile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alt` | query | `string` | no | default: 'json'.  Media, and proto also available. |
| `$.xgafv` | query | `string` | no | E(x)tended (G)oogle (A)PI (F)ormat (V)ersion. This is an error format version parameter. The parameter determines the format of error messages returned by the API. Options are (1) legacy error format or (2) the standard error format with enhanced error detail. |
