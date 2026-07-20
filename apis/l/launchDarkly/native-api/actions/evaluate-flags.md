# Evaluate Flags with LaunchDarkly

Evaluates feature flags for a LaunchDarkly context.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectKey/environments/:environmentKey/flags/evaluate`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Evaluate Flags](https://launchdarkly.com/docs/api/contexts/evaluate-context-instance)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
