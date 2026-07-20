# Get Environment with LaunchDarkly

Retrieves an environment from LaunchDarkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectKey/environments/:environmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Get Environment](https://launchdarkly.com/docs/api/environments/get-environment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
