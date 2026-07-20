# List Segments with LaunchDarkly

Retrieves segments from LaunchDarkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/segments/:projectKey/:environmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [List Segments](https://launchdarkly.com/docs/api/segments/get-segments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
