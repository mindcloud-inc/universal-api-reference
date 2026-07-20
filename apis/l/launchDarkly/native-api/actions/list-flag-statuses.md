# List Flag Statuses with LaunchDarkly

Retrieves feature flag statuses from LaunchDarkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/flag-statuses/:projectKey/:environmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [List Flag Statuses](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag-statuses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
