# Get Contact with Benchmark Email

Retrieves a contact from a Benchmark Email contact list.

## Endpoint

- **Method:** `GET`
- **Path:** `/Contact/:listId/ContactDetails/:id`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Get Contact](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Benchmark contact ID within the list. |
| `listId` | path | `string` | yes | Benchmark contact list ID. |
