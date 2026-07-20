# Search Events with Metronome

Finds events in Metronome by transaction ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events/search`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Search Events](https://docs.metronome.com/api-reference/usage/search-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionIds[]` | body | `array<string>` | yes | The transaction IDs of the events to retrieve. Send multiple values as a array. |
