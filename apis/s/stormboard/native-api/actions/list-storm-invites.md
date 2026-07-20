# List Storm Invites with Stormboard

Retrieves your Storm invites from Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/storms/invites`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [List Storm Invites](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `needle` | query | `string` | no | Filter invites by storm title text. |
| `team` | query | `number` | no | Filter invites by team ID. |
