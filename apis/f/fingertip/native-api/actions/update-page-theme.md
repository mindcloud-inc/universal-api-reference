# Update Page Theme with Fingertip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/pages/:pageId/theme`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Update Page Theme](https://docs.fingertip.com/openapi-specs/update-page-theme)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `object` | no | Theme content configuration |
| `pageId` | path | `string` | yes | ID of the page to update the theme for |
