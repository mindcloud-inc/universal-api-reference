# Get Flag Status with LaunchDarkly

Retrieves a feature flag status across LaunchDarkly environments.

## Endpoint

- **Method:** `GET`
- **Path:** `/flag-status/:projectKey/:featureFlagKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Get Flag Status](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag-status-across-environments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureFlagKey` | path | `string` | yes | The LaunchDarkly feature flag key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
