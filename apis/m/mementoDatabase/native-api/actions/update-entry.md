# Update Entry with Memento Database

Updates an existing entry in a Memento Database library.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/libraries/[:libraryId]/entries/[:entryId]`
- **Base URL:** `https://api.mementodatabase.com/v1`
- **Official documentation:** [Update Entry](https://mementodatabase.docs.apiary.io/#reference/0/entry/edit-an-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `libraryId` | path | `string` | yes | The ID of the library. |
| `entryId` | path | `string` | yes | The ID of the entry. |
| `fields[]` | body | `array<object>` | yes | An array of field objects to update. Example: [{"id":1,"value":"Updated"}] |
