# Create Event Dump Job with UniOne

Creates an event dump job in UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `event-dump/create.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Create Event Dump Job](https://docs.unione.io/en/web-api-ref#event-dump-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_time` | body | `string` | yes | UTC start of the dump window in YYYY-MM-DD hh:mm:ss format. |
| `limit` | body | `number` | no | Maximum number of events returned to the dump job. |
