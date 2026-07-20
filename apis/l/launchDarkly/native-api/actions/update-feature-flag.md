# Update Feature Flag with LaunchDarkly

Updates an existing feature flag in LaunchDarkly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/flags/:projectKey/:featureFlagKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Update Feature Flag](https://launchdarkly.com/docs/api/feature-flags/patch-feature-flag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureFlagKey` | path | `string` | yes | The LaunchDarkly feature flag key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
