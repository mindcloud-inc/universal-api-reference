# List Post History with RecurPost

Retrieves post history from RecurPost by social account.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/history_data`
- **Base URL:** `https://social.recurpost.com`
- **Official documentation:** [List Post History](https://developers.recurpost.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | body | `string` | no | End date for filtering history in Y-m-d H:i:s format. |
| `id` | body | `string` | yes | Social account ID from List Social Accounts. |
| `is_get_video_updates` | body | `boolean` | no | Include video posts in the response. |
| `start_date` | body | `string` | no | Start date for filtering history in Y-m-d H:i:s format. |
