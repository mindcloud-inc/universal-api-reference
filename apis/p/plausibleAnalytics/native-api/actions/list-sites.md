# List Sites with Plausible Analytics

Retrieves accessible sites from Plausible Analytics.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/sites`
- **Base URL:** `https://plausible.io`
- **Official documentation:** [List Sites](https://plausible.io/docs/sites-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of sites to return. Defaults to 100 in Plausible. |
| `team_id` | query | `string` | no | Optional team identifier to scope the sites list. |
