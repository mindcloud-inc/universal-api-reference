# List Package Issues with Snyk

Retrieves package issues from Snyk by package URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_id/packages/:purl/issues`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List Package Issues](https://docs.snyk.io/snyk-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purl` | path | `string` | yes | Package URL for the request path. |
