# List Group Client Members with CoachAccountable

Retrieves group client members from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Group Client Members](https://www.coachaccountable.com/APIDocs#Group.getAllClientMembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GroupID` | body | `number` | yes | The ID of the Group whose Client Members are to be gotten. |
| `includeInactive` | body | `boolean` | no | Include Group Clients who are inactive. |
