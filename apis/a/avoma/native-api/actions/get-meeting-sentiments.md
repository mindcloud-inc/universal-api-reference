# Get Meeting Sentiments with Avoma

Retrieves sentiments for a meeting from Avoma.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/meeting_sentiments/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Get Meeting Sentiments](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_uuid` | query | `string` | yes | Unique ID of the meeting for which sentiments will be fetched. |
