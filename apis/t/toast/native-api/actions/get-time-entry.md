# Get Time Entry with Toast

Retrieves one employee time entry by Toast GUID or external identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/timeEntries/:timeEntryId`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [Get Time Entry](https://doc.toasttab.com/openapi/labor/operation/timeEntriesTimeEntryIdGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeEntryId` | path | `string` | yes | The Toast GUID or external identifier of the time entry. |
| `includeMissedBreaks` | query | `boolean` | no | Include missed breaks in the time entry break array. |
| `includeArchived` | query | `boolean` | no | Return the time entry when it is archived. |
