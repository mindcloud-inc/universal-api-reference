# Create Sequence with Steps with Sequenzy

Creates a sequence with explicit steps in Sequenzy.

## Endpoint

- **Method:** `POST`
- **Path:** `/sequences`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Create Sequence with Steps](https://docs.sequenzy.com/api-reference/sequences/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventName` | body | `string` | yes | Trigger event name. |
| `name` | body | `string` | yes | Sequence name. |
