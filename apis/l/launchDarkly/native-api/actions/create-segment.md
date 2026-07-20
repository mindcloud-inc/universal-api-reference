# Create Segment with LaunchDarkly

Creates a new segment in LaunchDarkly.

## Endpoint

- **Method:** `POST`
- **Path:** `/segments/:projectKey/:environmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Create Segment](https://launchdarkly.com/docs/api/segments/post-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
