# Get Organization with Buildkite

Retrieves an organization from Buildkite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization`
- **Base URL:** `https://api.buildkite.com/v2`
- **Official documentation:** [Get Organization](https://buildkite.com/docs/apis/rest-api/organizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | path | `string` | yes | The Buildkite organization slug. |
