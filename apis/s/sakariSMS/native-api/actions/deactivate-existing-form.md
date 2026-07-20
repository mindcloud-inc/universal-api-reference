# Deactivate Existing Form with Sakari SMS

Deactivates an existing lead form in Sakari SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/accounts/:accountId/forms/:formId/deactivate`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Deactivate Existing Form](https://developer.sakari.io/api-reference/forms/deactivate-an-existing-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | yes |
