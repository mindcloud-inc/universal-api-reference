# List Lead Form Templates with Sakari SMS

Retrieves lead form templates from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/forms/templates`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Lead Form Templates](https://developer.sakari.io/api-reference/forms/fetch-all-lead-form-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | General search term that searchs accross multiple fields |
| `orderBy` | query | `string` | no | Sort the return results |
