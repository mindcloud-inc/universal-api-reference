# Get Journal Entries with ServiceTitan

Gets a list of journal entries.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/journal-entries`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Journal Entries](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/JournalEntries_GetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Comma-delimited list of journal entry IDs, maximum 50 items |
