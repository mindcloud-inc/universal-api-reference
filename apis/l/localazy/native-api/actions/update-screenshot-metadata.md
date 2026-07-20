# Update Screenshot Metadata with Localazy

Updates screenshot tags, phrases, or metadata in Localazy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/screenshots/:screenshotId`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Update Screenshot Metadata](https://localazy.com/docs/api/screenshot-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |
| `screenshotId` | path | `string` | yes | Identifier of the screenshot to update. |
| `comment` | body | `string` | no | Custom screenshot description. |
| `addTags[]` | body | `array<string>` | no | Tags to add to the screenshot. |
| `removeTags[]` | body | `array<string>` | no | Tags to remove from the screenshot. |
| `tags[]` | body | `array<string>` | no | Replacement tag list for the screenshot. |
| `addPhrases[]` | body | `array<string>` | no | Phrase identifiers to add to the screenshot. |
| `removePhrases[]` | body | `array<string>` | no | Phrase identifiers to remove from the screenshot. |
| `phrases[]` | body | `array<string>` | no | Replacement phrase identifier list for the screenshot. |
| `addMetadata` | body | `object` | no | Metadata entries to add. |
| `removeMetadata[]` | body | `array<string>` | no | Metadata keys to remove. |
| `metadata` | body | `object` | no | Replacement metadata object. |
