# Create Channel Gate with Smart Sender

Creates a channel gateway in Smart Sender, or returns the existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/channels/:channelId/gates`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Create Channel Gate](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676444598/Channels%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The Smart Sender channel ID. |
| `firstName` | body | `string` | no | First name for the created gateway contact. |
| `identifier` | body | `string` | yes | Messenger identifier for the contact gateway. |
