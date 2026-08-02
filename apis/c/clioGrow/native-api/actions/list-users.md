# List Users with Clio Grow

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [List Users](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Users/operation/User%23index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_since` | query | `date` | no | Only include users created on or after this ISO-8601 timestamp. |
| `updated_since` | query | `date` | no | Only include users updated on or after this ISO-8601 timestamp. |
