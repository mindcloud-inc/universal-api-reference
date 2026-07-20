# Add Client to Group with CoachAccountable

Adds a client to a CoachAccountable group.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Add Client to Group](https://www.coachaccountable.com/APIDocs#Group.addClientMember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client to be added. |
| `GroupID` | body | `number` | yes | The ID of the Course to which the Client is to be added. |
