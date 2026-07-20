# Get Longreads Recommendations with Longreads

Retrieves Longreads article recommendations by topic.

## Endpoint

- **Method:** `GET`
- **Path:** `/longreads/v1/recommendations`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Get Longreads Recommendations](https://longreads.com/wp-json/longreads/v1/recommendations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topics` | query | `string` | yes | Comma-separated topics such as books or climate. |
