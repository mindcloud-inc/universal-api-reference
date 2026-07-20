# Update Contact with Benchmark Email

Updates a contact in a Benchmark Email contact list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Contact/:listId/ContactDetails/:contactId`
- **Base URL:** `https://clientapi.benchmarkemail.com`
- **Official documentation:** [Update Contact](https://developer.benchmarkemail.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Benchmark contact ID. |
| `Data` | body | `object` | yes | Contact payload object. |
| `listId` | path | `string` | yes | Benchmark contact list ID. |
