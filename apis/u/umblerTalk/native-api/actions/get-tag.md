# Get Tag with Umbler Talk

Retrieves a tag from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tags/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Get Tag](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The tag ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
