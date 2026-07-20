# List History with Minelead

Retrieves search history from your Minelead account.

## Endpoint

- **Method:** `GET`
- **Path:** `/history`
- **Base URL:** `https://api.minelead.io/v1`
- **Official documentation:** [List History](https://api.minelead.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | yes | History offset to start from. |
| `limit` | query | `number` | yes | Maximum number of history records to return. |
