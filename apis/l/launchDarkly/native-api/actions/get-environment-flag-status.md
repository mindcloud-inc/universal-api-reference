# Get Environment Flag Status with LaunchDarkly

Retrieves a feature flag status for one LaunchDarkly environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/flag-statuses/:projectKey/:environmentKey/:featureFlagKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Get Environment Flag Status](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `featureFlagKey` | path | `string` | yes | The LaunchDarkly feature flag key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
