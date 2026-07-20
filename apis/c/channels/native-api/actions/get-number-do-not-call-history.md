# Get Number Do Not Call History with Channels

Retrieves do-not-call history for a phone number in Channels.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/dnclist/{msisdn}`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Get Number Do Not Call History](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | path | `string` | yes | Phone number whose Do Not Call List history should be returned. |
