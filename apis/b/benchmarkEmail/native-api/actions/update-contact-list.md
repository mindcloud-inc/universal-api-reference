# Update Contact List with Benchmark Email

Updates an existing contact list in Benchmark Email.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Contact/:listId`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Update Contact List](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Data` | body | `object` | yes | Updated list name. |
| `listId` | path | `string` | yes | Benchmark contact list ID. |
