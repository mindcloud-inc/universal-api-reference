# List Agreements with CoachAccountable

Retrieves agreements from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Agreements](https://www.coachaccountable.com/APIDocs#Agreement.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter to Agreements belonging to a specific client. |
| `title` | body | `string` | no | Filter Agreements by which title, prefixed. |
| `includeContent` | body | `boolean` | no | Set to true to include the full HTML content of the Agreements. |
| `which` | body | `list` | no | Filter by Agreement status. Accepted values: `A`, `B`, `O`. |
| `dateFrom` | body | `date` | no | Set to restrict Agreements returned to those issued at or after the provided value. |
| `dateTo` | body | `date` | no | Set to restrict Agreements returned to those issued at or before the provided value. |
