# List Group Coach Members with CoachAccountable

Retrieves group coach members from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Group Coach Members](https://www.coachaccountable.com/APIDocs#Group.getAllCoachMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GroupID` | body | `number` | yes | The ID of the Group whose Coach Members are to be gotten. |
| `includeInactive` | body | `boolean` | no | Include Group Coaches who are inactive. |
