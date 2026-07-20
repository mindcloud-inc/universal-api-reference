# Create Email Template with SendX

## Endpoint

- **Method:** `POST`
- **Path:** `/template/email`
- **Base URL:** `https://api.sendx.io/api/v1/rest`
- **Official documentation:** [Create Email Template](https://docs.sendx.io/api-reference/template/create-email-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `subject` | body | `string` | yes |
| `htmlCode` | body | `string` | no |
| `templateCode` | body | `string` | no |
| `editorType` | body | `number` | no |
