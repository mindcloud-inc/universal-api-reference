# Edit Message with Umbler Talk

Updates an existing message in Umbler Talk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/messages/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Edit Message](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The message ID. |
| `newMessage` | body | `string` | yes | Updated message text. |
| `organizationId` | query | `string` | yes | The organization ID. |
