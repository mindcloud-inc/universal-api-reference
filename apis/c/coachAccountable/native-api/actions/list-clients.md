# List Clients with CoachAccountable

Retrieves clients from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Clients](https://www.coachaccountable.com/APIDocs#Client.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeInactive` | body | `boolean` | no | Set to true to include Clients that are currently marked inactive. |
| `CompanyID` | body | `number` | no | Get only Clients who are belong to a given Company. Provide a zero to get clients that don't belong to any Company. |
| `sortOption` | body | `list` | no | Accepted values: `A`, `C`. |
