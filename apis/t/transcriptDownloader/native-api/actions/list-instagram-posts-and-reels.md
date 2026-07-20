# List Instagram Posts and Reels with Transcript Downloader

Retrieves Instagram posts and reels from Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/instagram/list`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [List Instagram Posts and Reels](https://documentation.transcriptdownloader.com/instagram-api#get-all-posts--reels-list-of-the-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | The list ID returned by the Instagram profile action. |
| `max_age_days` | body | `number` | no | Only return posts and reels newer than this many days. |
| `include_webhook` | body | `string` | no | A public webhook URL to receive the completed result. |
