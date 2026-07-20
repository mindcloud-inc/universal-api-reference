# Retrieve Group Invite with Rownd Data Privacy

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group/invites/:invite`
- **Base URL:** `https://api.rownd.io/applications/{appId}`
- **Official documentation:** [Retrieve Group Invite](https://docs.rownd.io/api-reference/groups/platform/invites/invite-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `string` | yes | Rownd group identifier. |
| `invite` | path | `string` | yes | Rownd group invite identifier. |
