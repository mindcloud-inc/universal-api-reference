# Delete Datalist Entry Item with Global Patron

Deletes a datalist entry item from Global Patron.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/restricted/datalist/{datalistId}/entry/{datalistEntryId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Delete Datalist Entry Item](https://www.globalpatron.com/developers/api/datalists/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datalistId` | path | `string` | yes | ID of the datalist. |
| `datalistEntryId` | path | `string` | yes | ID of the datalist entry item to delete. |
