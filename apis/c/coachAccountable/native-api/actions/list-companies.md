# List Companies with CoachAccountable

Retrieves companies from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Companies](https://www.coachaccountable.com/APIDocs#Company.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeInactive` | body | `boolean` | no | Set to true to include Companies that are marked inactive. |
| `sortOption` | body | `list` | no | Accepted values: `A`, `C`. |
