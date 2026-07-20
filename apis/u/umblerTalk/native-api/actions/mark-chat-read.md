# Mark Chat Read with Umbler Talk

Marks a chat as read in Umbler Talk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/chats/[:id]/read/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Mark Chat Read](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The chat ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
