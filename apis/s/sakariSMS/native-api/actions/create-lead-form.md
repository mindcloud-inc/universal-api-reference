# Create Lead Form with Sakari SMS

Creates a new lead form in Sakari SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/forms`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Create Lead Form](https://developer.sakari.io/api-reference/forms/create-lead-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | query | `string` | no | Id of the form template you wish to clone |
| `name` | body | `string` | yes | — |
