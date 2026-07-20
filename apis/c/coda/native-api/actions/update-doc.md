# Update Doc with Coda

Updates metadata for a Coda doc.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/docs/:docId`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [Update Doc](https://coda.io/developers/apis/v1#tag/Docs/operation/updateDoc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `docId` | path | `list` | yes |
| `title` | body | `string` | no |
| `iconName` | body | `string` | no |
