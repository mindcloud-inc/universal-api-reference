# Forward Message with Umbler Talk

Forwards a message in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/[:id]/forward/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Forward Message](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | body | `string` | yes | Destination chat ID. |
| `id` | path | `string` | yes | The message ID to forward. |
| `organizationId` | body | `string` | yes | The organization ID. |
