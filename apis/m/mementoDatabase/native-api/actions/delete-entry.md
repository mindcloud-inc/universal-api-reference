# Delete Entry with Memento Database

Deletes an existing entry from a Memento Database library.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/libraries/[:libraryId]/entries/[:entryId]`
- **Base URL:** `https://api.mementodatabase.com/v1`
- **Official documentation:** [Delete Entry](https://mementodatabase.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `libraryId` | path | `string` | yes | The ID of the library. |
| `entryId` | path | `string` | yes | The ID of the entry. |
