# Create Invite with Tally

## Endpoint

- **Method:** `POST`
- **Path:** `organizations/:organizationId/invites`
- **Base URL:** `https://api.tally.so`
- **Official documentation:** [Create Invite](https://developers.tally.so/api-reference/endpoint/organizations/invites/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `list<string>` | yes | — |
| `workspaceIds` | body | `list` | yes | Send multiple values as a array. |
| `emails` | body | `string` | yes | Send multiple values as a array. |
