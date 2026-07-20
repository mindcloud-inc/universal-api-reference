# Update Chat with Umbler Talk

Updates an existing chat in Umbler Talk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/chats/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Update Chat](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The chat ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
