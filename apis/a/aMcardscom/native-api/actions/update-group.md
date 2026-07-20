# Update Group with AMcards.com

Updates an existing contact group in AMcards.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/group/:groupId/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [Update Group](https://staging.amcards.com/docs/developers-only/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | no | AMcards group identifier from the `/group/` resource URI. |
| `name` | body | `string` | no | Updated name for the group. |
