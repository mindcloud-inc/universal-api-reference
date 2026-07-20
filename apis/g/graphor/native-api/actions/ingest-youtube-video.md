# Ingest YouTube Video with Graphor

Creates a new source in Graphor from a YouTube video.

## Endpoint

- **Method:** `POST`
- **Path:** `/ingest-youtube`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Ingest YouTube Video](https://docs.graphorlm.com/api-reference/sources/upload#ingest-youtube)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The YouTube video URL to ingest. |
