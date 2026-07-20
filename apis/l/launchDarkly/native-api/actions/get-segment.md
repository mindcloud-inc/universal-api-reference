# Get Segment with LaunchDarkly

Retrieves a segment from LaunchDarkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/segments/:projectKey/:environmentKey/:segmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Get Segment](https://launchdarkly.com/docs/api/segments/get-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
| `segmentKey` | path | `string` | yes | The LaunchDarkly segment key. |
