# Retrieve Email Opens with Cloze

Retrieves email opens from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages/opens`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Retrieve Email Opens](https://api.cloze.com/api-docs/#/paths/v1-messages-opens/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `number` | no | UTC milliseconds timestamp for first message to retrieve. |
