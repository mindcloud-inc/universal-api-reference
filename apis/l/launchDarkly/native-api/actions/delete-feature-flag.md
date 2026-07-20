# Delete Feature Flag with LaunchDarkly

Deletes an existing feature flag from LaunchDarkly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/flags/:projectKey/:featureFlagKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Delete Feature Flag](https://launchdarkly.com/docs/api/feature-flags/delete-feature-flag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureFlagKey` | path | `string` | yes | The LaunchDarkly feature flag key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
