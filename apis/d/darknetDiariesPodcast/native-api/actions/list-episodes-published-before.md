# List Episodes Published Before with Darknet Diaries Podcast

Retrieves podcast episodes published before a date from Darknet Diaries Podcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://podcast.darknetdiaries.com`
- **Official documentation:** [List Episodes Published Before](https://podcast.darknetdiaries.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publishedBefore` | query | `date` | yes | Only include episodes published before this date. |
