# Copy Feature Flag with LaunchDarkly

Copies feature flag settings between LaunchDarkly environments.

## Endpoint

- **Method:** `POST`
- **Path:** `/flags/:projectKey/:featureFlagKey/copy`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Copy Feature Flag](https://launchdarkly.com/docs/api/feature-flags/copy-feature-flag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureFlagKey` | path | `string` | yes | The LaunchDarkly feature flag key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
