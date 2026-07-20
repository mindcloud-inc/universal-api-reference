# Get Event Dump Job with UniOne

Retrieves an event dump job from UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `event-dump/get.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Get Event Dump Job](https://docs.unione.io/en/web-api-ref#event-dump-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dump_id` | body | `string` | yes | Dump identifier returned by Create Event Dump Job. |
