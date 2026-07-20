# Create editor session with CraftMyPDF

Creates an editor session in CraftMyPDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-editor-session`
- **Base URL:** `https://api.craftmypdf.com/v1`
- **Official documentation:** [Create editor session](https://craftmypdf.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | body | `string` | yes |
| `expiration` | body | `number` | yes |
| `canSave` | body | `boolean` | no |
| `canCreatePDF` | body | `boolean` | no |
| `canViewSettings` | body | `boolean` | no |
| `canPreview` | body | `boolean` | no |
| `canEditJSON` | body | `boolean` | no |
| `canShowHeader` | body | `boolean` | no |
| `canShowLayers` | body | `boolean` | no |
| `canShowPropertyPanel` | body | `boolean` | no |
| `canShowHelp` | body | `boolean` | no |
| `canShowData` | body | `boolean` | no |
| `canShowExpressionDoc` | body | `boolean` | no |
| `canShowPropertyBinding` | body | `boolean` | no |
| `canShowBackURL` | body | `boolean` | no |
| `jsonMode` | body | `number` | no |
| `backURL` | body | `string` | no |
