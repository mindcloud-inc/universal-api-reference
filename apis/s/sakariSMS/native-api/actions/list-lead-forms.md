# List Lead Forms with Sakari SMS

Retrieves lead forms from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/forms`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Lead Forms](https://developer.sakari.io/api-reference/forms/fetch-all-lead-forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | General search term that searchs accross multiple fields |
| `orderBy` | query | `string` | no | Sort the return results |
