# Add Feed with Inoreader

Adds a new feed subscription in Inoreader.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription/quickadd`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [Add Feed](https://www.inoreader.com/developers/add-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quickadd` | body | `string` | yes | Feed URL to follow. |
