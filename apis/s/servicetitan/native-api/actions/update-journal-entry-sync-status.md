# Update Journal Entry Sync Status with ServiceTitan

Updates the sync status of a journal entry, for example marking it Synced after exporting it to an accounting system.

## Endpoint

- **Method:** `PATCH`
- **Path:** `accounting/v2/tenant/{tenant}/journal-entries/:id/sync`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Journal Entry Sync Status](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/JournalEntries_SyncUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `syncStatus` | body | `list<string>` | yes | Accepted values: `Error`, `Excluded`, `InProgress`, `NotSynced`, `OutOfSync`, `Synced`. |
| `versionId` | body | `number` | no | The journal entry version that was synced. Required when Sync Status is Synced; ignored otherwise. |
| `message` | body | `string` | no | Message about the new sync state, such as the external reference or an error. |
| `customFields` | body | `object` | no | Custom fields to create or update, as name/value pairs. Maximum 5 per journal entry. |
