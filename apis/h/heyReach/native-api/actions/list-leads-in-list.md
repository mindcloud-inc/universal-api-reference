# List Leads In List with Hey Reach

Retrieves leads from a Hey Reach list.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/list/GetLeadsFromList`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [List Leads In List](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `listId` | body | `number` | yes |
| `offset` | body | `number` | no |
| `keyword` | body | `string` | no |
| `leadProfileUrl` | body | `string` | no |
| `leadLinkedInId` | body | `string` | no |
| `limit` | body | `number` | no |
| `createdFrom` | body | `date` | no |
| `createdTo` | body | `date` | no |
