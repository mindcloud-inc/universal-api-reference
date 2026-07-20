# Update Environment with LaunchDarkly

Updates an existing environment in LaunchDarkly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectKey/environments/:environmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Update Environment](https://launchdarkly.com/docs/api/environments/patch-environment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
