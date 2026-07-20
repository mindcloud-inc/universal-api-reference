# List Contacts By Points with UpViral

Retrieves campaign contacts from UpViral by points.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://app.upviral.com/api/v1/`
- **Official documentation:** [List Contacts By Points](https://www.upviral.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The UpViral campaign ID to search contacts in. |
| `operator` | body | `list` | yes | Comparison operator for points, such as <, >, or =. Accepted values: `0`, `1`, `2`. |
| `points` | body | `number` | yes | Point value to compare against. |
