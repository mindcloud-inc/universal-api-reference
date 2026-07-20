# List Collection Projects with Snyk

Retrieves projects from a Snyk collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/collections/:collection_id/relationships/projects`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List Collection Projects](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Snyk collection ID for the request path. |
