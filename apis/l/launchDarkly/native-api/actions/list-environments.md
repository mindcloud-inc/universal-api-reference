# List Environments with LaunchDarkly

Retrieves environments from LaunchDarkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectKey/environments`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [List Environments](https://launchdarkly.com/docs/api/environments/get-environments-by-project)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
