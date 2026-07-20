# Create Recordings Archive Link with Channels

Creates a recordings archive link in Channels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/archive`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Create Recordings Archive Link](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `date` | yes | Lower bound for call recordings to include in the archive. |
| `dateTo` | body | `date` | yes | Upper bound for call recordings to include in the archive. |
| `msisdns[]` | body | `array<string>` | no | Optional phone numbers to include in the recordings archive. Send multiple values as a array. |
| `userIds[]` | body | `array<number>` | no | Optional user IDs participating in calls to include in the archive. Send multiple values as a array. |
