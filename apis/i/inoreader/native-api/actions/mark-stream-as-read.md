# Mark Stream As Read with Inoreader

Marks an Inoreader stream as read.

## Endpoint

- **Method:** `POST`
- **Path:** `/mark-all-as-read`
- **Base URL:** `https://www.inoreader.com/reader/api/0`
- **Official documentation:** [Mark Stream As Read](https://www.inoreader.com/developers/mark-all-as-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | body | `string` | yes | Stream ID to mark as read. |
| `ts` | body | `number` | yes | Unix timestamp in seconds or microseconds from the last displayed fetch. |
