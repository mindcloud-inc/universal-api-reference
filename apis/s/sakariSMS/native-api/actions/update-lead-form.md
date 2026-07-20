# Update Lead Form with Sakari SMS

Updates an existing lead form in Sakari SMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/accounts/:accountId/forms/:formId`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Update Lead Form](https://developer.sakari.io/api-reference/forms/update-lead-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `formId` | path | `string` | yes |
| `name` | body | `string` | yes |
