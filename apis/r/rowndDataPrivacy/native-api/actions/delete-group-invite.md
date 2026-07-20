# Delete Group Invite with Rownd Data Privacy

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:group/invites/:invite`
- **Base URL:** `https://api.rownd.io/applications/{appId}`
- **Official documentation:** [Delete Group Invite](https://docs.rownd.io/api-reference/groups/platform/invites/invite-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Rownd group identifier. |
| `invite` | path | `string` | yes | Rownd group invite identifier. |
