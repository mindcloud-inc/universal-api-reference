# Get Media File with Wbiztool

Retrieves a specific media file from Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/media/{{media_id}}/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Get Media File](https://wbiztool.com/docs/media-get-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_id` | path | `number` | yes | Media file ID to fetch in the URL path. |
