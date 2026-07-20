# Create Contact Segment with Benchmark Email

Creates a contact segment in Benchmark Email.

## Endpoint

- **Method:** `POST`
- **Path:** `/Contact/:listId/Segments`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Create Contact Segment](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactIDs` | body | `string<string>` | yes | Contact IDs to include in the segment. |
| `listId` | path | `string` | yes | Benchmark contact list ID. |
