# Send Inbox Alias Verification Code with ThriveDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/settings/inbox/{{inboxId}}/aliases/{{aliasId}}/send-code`
- **Base URL:** `https://api.thrivedesk.com`
- **Official documentation:** [Send Inbox Alias Verification Code](https://documenter.getpostman.com/view/13910051/2sB2qUnQcP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aliasId` | path | `string` | yes | The alias ID. |
| `inboxId` | path | `string` | yes | The inbox ID. |
