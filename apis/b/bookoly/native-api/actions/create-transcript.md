# Create Transcript with Bookoly

Creates a transcript from audio or video in Bookoly.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-transcript`
- **Base URL:** `https://bookoly.com/api/v1`
- **Official documentation:** [Create Transcript](https://bookoly.com/docs/api/v1#/paths/~1create-transcript/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcript` | body | `object` | yes | Object containing the transcript job settings from the Bookoly docs. |
