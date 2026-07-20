# List Episodes By Date Range with Darknet Diaries Podcast

Retrieves podcast episodes in a date range from Darknet Diaries Podcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://podcast.darknetdiaries.com`
- **Official documentation:** [List Episodes By Date Range](https://podcast.darknetdiaries.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publishedAfter` | query | `date` | yes | Start date for the published date range. |
| `publishedBefore` | query | `date` | yes | End date for the published date range. |
