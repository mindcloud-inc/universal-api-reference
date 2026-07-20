# List Channels with SurveySparrow

Retrieves all channels from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [List Channels](https://developers.surveysparrow.com/rest-apis/get-v-3-channels/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | query | `number` | yes | ID of the survey |
| `type` | query | `list` | no | Type of channel |
