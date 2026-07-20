# Update Segment with LaunchDarkly

Updates an existing segment in LaunchDarkly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/segments/:projectKey/:environmentKey/:segmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Update Segment](https://launchdarkly.com/docs/api/segments/patch-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
| `segmentKey` | path | `string` | yes | The LaunchDarkly segment key. |
