# Research with You.com

Retrieves a research report from You.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/research`
- **Base URL:** `https://api.you.com`
- **Official documentation:** [Research](https://docs.you.com/api-reference/research/v1-research)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Research question or complex query. |
| `research_effort` | body | `string` | no | How deeply the API should research. |
