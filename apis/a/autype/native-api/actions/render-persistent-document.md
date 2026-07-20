# Render Persistent Document with Autype

Creates a persistent document render job in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/render/document/{documentId}`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Render Persistent Document](https://docs.autype.com/api-reference/developer-api/render-persistent-document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `documentId` | path | `string` | yes |
| `format` | body | `string` | no |
| `variables` | body | `object` | no |
| `webhook` | body | `object` | no |
