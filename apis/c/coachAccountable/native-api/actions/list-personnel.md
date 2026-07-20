# List Personnel with CoachAccountable

Retrieves personnel from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Personnel](https://www.coachaccountable.com/APIDocs#Personnel.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeInactive` | body | `boolean` | no | Set to true to include Personnel that are marked inactive. |
| `sortOption` | body | `list` | no | Accepted values: `A`, `C`. |
