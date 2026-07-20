# List Sessions with CoachAccountable

Retrieves sessions from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Sessions](https://www.coachaccountable.com/APIDocs#Session.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter Sessions by Client. |
| `dateFrom` | body | `date` | no | Set to restrict Sessions returned to those at or after the provided value. |
| `dateTo` | body | `date` | no | Set to restrict Sessions returned to those at or before the provided value. |
| `includeDrafts` | body | `boolean` | no | Set to true to include Sessions not yet marked complete. |
| `sortField` | body | `list` | no | Accepted values: `dateAdded`, `dateDone`, `dateOf`. |
| `sortDirection` | body | `list` | no | Accepted values: `A`, `D`. |
