# Update Tag with Umbler Talk

Updates an existing tag in Umbler Talk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/tags/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Update Tag](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The tag ID. |
| `name` | body | `string` | no | Tag name. |
| `organizationId` | query | `string` | yes | The organization ID. |
