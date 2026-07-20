# Create Media Safety Screening with InsightIQ

Creates a media safety screening in InsightIQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/safety/media-screening`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Media Safety Screening](https://docs.insightiq.ai/docs/api-reference/api/ref)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Caption or description of the media |
| `flagging_criteria_id` | body | `string` | no | Optional flagging criteria override |
| `media_type` | body | `string` | yes | Media type: IMAGE or VIDEO |
| `media_url` | body | `string` | yes | Publicly accessible media URL |
