# Get Collection with Snyk

Retrieves a collection from a Snyk organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/collections/:collection_id`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [Get Collection](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | path | `string` | yes | Snyk collection ID for the request path. |
