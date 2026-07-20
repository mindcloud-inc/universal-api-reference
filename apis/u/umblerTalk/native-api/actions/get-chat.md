# Get Chat with Umbler Talk

Retrieves a chat from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Get Chat](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The chat ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
