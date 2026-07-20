# Retrieve sending nodes from Mumara with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/mumara/sending-nodes`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Retrieve sending nodes from Mumara](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter nodes by status |
| `include_stats` | query | `boolean` | no | Include delivery statistics for each node |
