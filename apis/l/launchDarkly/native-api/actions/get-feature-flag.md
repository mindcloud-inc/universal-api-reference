# Get Feature Flag with LaunchDarkly

Retrieves a feature flag from LaunchDarkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/flags/:projectKey/:featureFlagKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Get Feature Flag](https://launchdarkly.com/docs/api/feature-flags/get-feature-flag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureFlagKey` | path | `string` | yes | The LaunchDarkly feature flag key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
