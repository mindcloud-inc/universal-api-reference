# List Message States with Umbler Talk

Retrieves a message's state history from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages/[:id]/states/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Message States](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The message ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
