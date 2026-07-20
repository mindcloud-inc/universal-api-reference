# Get Message with Umbler Talk

Retrieves a message from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Get Message](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The message ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
