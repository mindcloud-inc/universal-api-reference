# List Campaigns with Sakari SMS

Retrieves account campaigns from Sakari SMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/campaigns`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [List Campaigns](https://developer.sakari.io/api-reference/campaigns/fetch-campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter by name or part of |
