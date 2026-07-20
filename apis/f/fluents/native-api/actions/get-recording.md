# Get Recording with Fluents

Retrieves a call recording from Fluents.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls/recording`
- **Base URL:** `https://api.fluents.ai/v1`
- **Official documentation:** [Get Recording](https://docs.fluents.ai/api-reference/calls/get-recording)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Fluents call ID for the MP3 recording. |
