# Get List Contacts with Wiza

Retrieves contacts for a Wiza list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:id/contacts`
- **Base URL:** `https://wiza.co/api`
- **Official documentation:** [Get List Contacts](https://docs.wiza.co/api-reference/lists/get-list-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the list whose contacts to fetch. |
| `segment` | query | `string` | no | Optional list segment to return. |
