# Add Lead Tags with Hey Reach

Adds tags to a lead in Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/lead/AddTags`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [Add Lead Tags](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `leadProfileUrl` | body | `string` | no |
| `leadLinkedInId` | body | `string` | no |
| `tags[]` | body | `array<string>` | yes |
| `createTagIfNotExisting` | body | `boolean` | no |
