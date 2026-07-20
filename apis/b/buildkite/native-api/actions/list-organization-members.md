# List Organization Members with Buildkite

Retrieves organization members from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization/members`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [List Organization Members](https://buildkite.com/docs/apis/rest-api/organizations/members)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
