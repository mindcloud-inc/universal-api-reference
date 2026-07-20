# List Feature Flags with LaunchDarkly

Retrieves feature flags from LaunchDarkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/flags/:projectKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [List Feature Flags](https://launchdarkly.com/docs/api/feature-flags/get-feature-flags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
