# Update a Link with Linkbreakers

Updates an existing link in Linkbreakers.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/links/:id`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Update a Link](https://linkbreakers.com/help/api/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the link to update. |
| `directoryId` | body | `string` | no | The directory to move the link into. |
| `directoryIdDelete` | body | `boolean` | no | Remove the link from its directory. |
| `fallbackDestination` | body | `string` | no | Fallback destination URL to use when workflow steps are broken. |
| `leadGoalDefinition` | body | `string` | no | The lead goal definition for the link. |
| `leadTargetDefinition` | body | `string` | no | The lead target definition for the link. |
| `name` | body | `string` | no | The new name of the link. |
| `pageThemeId` | body | `string` | no | Page theme ID to assign to the link. |
| `qrcodeTemplateId` | body | `string` | no | QR code template ID to assign to the link. |
| `qrcodeTemplateIdDelete` | body | `boolean` | no | Remove the QR code template ID from the link. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the link. |
| `tagsDelete` | body | `boolean` | no | Remove all tags from the link. |
