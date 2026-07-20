# Get Track Remixes with Audius

Retrieves remixes of an Audius track.

## Endpoint

- **Method:** `GET`
- **Path:** `/tracks/:track_id/remixes`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Get Track Remixes](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `track_id` | path | `string` | yes | A Track ID. |
| `limit` | query | `number` | no | The number of items to fetch. |
