# Get Entry with Memento Database

Retrieves an entry from a Memento Database library.

## Endpoint

- **Method:** `GET`
- **Path:** `/libraries/[:libraryId]/entries/[:entryId]`
- **Base URL:** `https://api.mementodatabase.com/v1`
- **Official documentation:** [Get Entry](https://mementodatabase.docs.apiary.io/#reference/0/entry/get-a-single-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `libraryId` | path | `string` | yes | The ID of the library. |
| `entryId` | path | `string` | yes | The ID of the entry. |
