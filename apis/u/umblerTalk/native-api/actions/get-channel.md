# Get Channel with Umbler Talk

Retrieves a channel from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/channels/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Get Channel](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The channel ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
