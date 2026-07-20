# Update Tag with EARLY

Updates a tag in EARLY.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/tags/:tagId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Tag](https://developers.early.app/#2baca20f-6988-4f14-8b4b-3fbcbb5a81b9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `string` | yes | Tag ID. |
| `label` | body | `string` | yes | Updated tag label. |
