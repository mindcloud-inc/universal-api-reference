# Create Feature Flag with LaunchDarkly

Creates a new feature flag in LaunchDarkly.

## Endpoint

- **Method:** `POST`
- **Path:** `/flags/:projectKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Create Feature Flag](https://launchdarkly.com/docs/api/feature-flags/post-feature-flag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
