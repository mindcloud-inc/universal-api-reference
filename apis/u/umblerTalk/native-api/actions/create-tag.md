# Create Tag with Umbler Talk

Creates a new tag in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tags/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Create Tag](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Tag color. |
| `name` | body | `string` | yes | Tag name. |
| `organizationId` | body | `string` | yes | The organization ID. |
