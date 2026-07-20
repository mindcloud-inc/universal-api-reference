# Generate podcast with Vadootv

Creates an AI podcast in Vadootv.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate_podcast`
- **Base URL:** `https://aiapi.vadoo.tv`
- **Official documentation:** [Generate podcast](https://docs.vadoo.tv/docs/guide/create-an-ai-podcast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | URL of the blog post or PDF. Required if text is not provided. |
| `text` | body | `string` | no | Raw text transcript or content. Required if url is not provided. |
| `name1` | body | `string` | yes | Name of the first speaker. |
| `name2` | body | `string` | yes | Name of the second speaker. |
| `voice1` | body | `string` | no | Voice for speaker 1. |
| `voice2` | body | `string` | no | Voice for speaker 2. |
| `language` | body | `string` | no | Language of the podcast. |
| `duration` | body | `list<string>` | no | Target duration code. Accepted values: `1-2`, `2-5`. |
| `tone` | body | `string` | no | Tone of the conversation. |
| `theme` | body | `string` | no | Caption theme when generating a video podcast. |
