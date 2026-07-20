# Create Contact with Benchmark Email

Creates a contact in a Benchmark Email contact list.

## Endpoint

- **Method:** `POST`
- **Path:** `/Contact/:listId/ContactDetails`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Create Contact](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Data` | body | `object` | yes | Contact payload object. |
| `listId` | path | `string` | yes | Benchmark contact list ID. |
