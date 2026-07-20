# Search Episodes and Transcripts with Talk Python To Me

Finds episodes and transcripts in Talk Python To Me.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://search.talkpython.fm/api`
- **Official documentation:** [Search Episodes and Transcripts](https://search.talkpython.fm/api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search text to look for in Talk Python episodes and transcript content. Use hyphen-separated words for multi-keyword searches, such as python-testing. |
