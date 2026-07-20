# Search Entries with Zenkit

Searches for items in Zenkit.

## Endpoint

- **Method:** `GET`
- **Path:** `/entries/search`
- **Base URL:** `https://zenkit.com/api/v1`
- **Official documentation:** [Search Entries](https://app.zenkit.com/docs/api/entries/get-api-v1-entries-search-query-limit-preferredlistids-excludelistentryuuids-searchinarchive-includerelatedlists-includerelatedworkspaces-includerelatedlistelements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `excludeListEntryUUIDs[]` | query | `array<string>` | yes | An array of list entry UUIDs to exclude from the search. |
| `includeRelatedListElements` | query | `boolean` | yes | If true, the result will include the list elements for the found entries. |
| `includeRelatedLists` | query | `boolean` | yes | If true, the result will include the lists where the entries were found. |
| `includeRelatedWorkspaces` | query | `boolean` | yes | If true, the result will include the workspaces where the entries were found. |
| `limit` | query | `number` | yes | The number of entries that will be returned. |
| `preferredListIds[]` | query | `array<string>` | yes | The IDs of the lists that should be searched first. |
| `query` | query | `string` | yes | The search string. |
| `searchInArchive` | query | `boolean` | yes | If true, deprecated entries will be searched. |
