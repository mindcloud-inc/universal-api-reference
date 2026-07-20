# List Organizations with Snyk

Retrieves organizations available to the current Snyk user.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs`
- **Base URL:** `https://api.snyk.io/rest`
- **Official documentation:** [List Organizations](https://docs.snyk.io/snyk-api/reference/orgs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `string` | no | Only return organizations within this group. |
