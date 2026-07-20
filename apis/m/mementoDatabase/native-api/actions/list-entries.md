# List Entries with Memento Database

Retrieves entries from a library in Memento Database.

## Endpoint

- **Method:** `GET`
- **Path:** `/libraries/[:libraryId]/entries`
- **Base URL:** `https://api.mementodatabase.com/v1`
- **Official documentation:** [List Entries](https://mementodatabase.docs.apiary.io/#reference/0/entries/list-entries-on-a-library)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `libraryId` | path | `string` | yes | The ID of the library. |
| `limit` | query | `number` | no | Maximum number of entries to return. |
| `pageToken` | query | `string` | no | Page token returned by a previous list response. |
| `createdAfter` | query | `string` | no | Only return entries created after this ISO-8601 timestamp. |
| `updatedAfter` | query | `string` | no | Only return entries updated after this ISO-8601 timestamp. |
