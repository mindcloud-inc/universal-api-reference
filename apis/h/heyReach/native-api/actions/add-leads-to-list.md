# Add Leads To List with Hey Reach

Adds leads to a list in Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/list/AddLeadsToListV2`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Add Leads To List](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `leads[]` | body | `array<object>` | yes |
| `listId` | body | `number` | yes |
