# Delete Invite or Team Member with Push by Techulus

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/management/v1/teams/invite`
- **Base URL:** `https://push.techulus.com`
- **Official documentation:** [Delete Invite or Team Member](https://docs.push.techulus.com/management-api-beta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | body | `string` | yes | Team API key supplied from the connection Team credential. |
| `email` | body | `string` | yes | Email address of the invite or team member to remove. |
