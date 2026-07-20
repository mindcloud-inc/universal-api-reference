# Create Group Invite with Rownd Data Privacy

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:group/invites`
- **Base URL:** `https://api.rownd.io/applications/{appId}`
- **Official documentation:** [Create Group Invite](https://docs.rownd.io/api-reference/groups/platform/invites/invite-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Invitee email address. |
| `group` | path | `string` | yes | Rownd group identifier. |
| `redirect_url` | body | `string` | no | Redirect target for the invite link. |
| `roles[]` | body | `array<string>` | yes | Roles granted by the invite. |
