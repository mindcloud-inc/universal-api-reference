# Create Entry with Memento Database

Creates a new entry in a Memento Database library.

## Endpoint

- **Method:** `POST`
- **Path:** `/libraries/[:libraryId]/entries`
- **Base URL:** `https://api.mementodatabase.com/v1`
- **Official documentation:** [Create Entry](https://mementodatabase.docs.apiary.io/#reference/0/entries/create-a-new-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `libraryId` | path | `string` | yes | The ID of the library. |
| `fields[]` | body | `array<object>` | yes | An array of field objects. Example: [{"id":1,"value":"Record 1"},{"id":2,"value":1000}] |
