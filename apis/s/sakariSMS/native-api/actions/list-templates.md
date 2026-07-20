# List Templates with Sakari SMS

Retrieves account templates from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/templates`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Templates](https://developer.sakari.io/api-reference/templates/fetch-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter by name or part of |
