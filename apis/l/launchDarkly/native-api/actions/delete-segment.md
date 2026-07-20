# Delete Segment with LaunchDarkly

Deletes an existing segment from LaunchDarkly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/segments/:projectKey/:environmentKey/:segmentKey`
- **Base URL:** `https://app.launchdarkly.com/api/v2`
- **Official documentation:** [Delete Segment](https://launchdarkly.com/docs/api/segments/delete-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentKey` | path | `string` | yes | The LaunchDarkly environment key. |
| `projectKey` | path | `string` | yes | The LaunchDarkly project key. |
| `segmentKey` | path | `string` | yes | The LaunchDarkly segment key. |
