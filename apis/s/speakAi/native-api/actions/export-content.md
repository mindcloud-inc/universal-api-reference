# Export Content with Speak Ai

Creates a content export in Speak Ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/:mediaType/export/:mediaId/:fileType`
- **Base URL:** `https://api.speakai.co/v1`
- **Official documentation:** [Export Content](https://docs.speakai.co/#fcdaa5ed-cd17-48ba-98c7-2a7af4e13ce6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mediaType` | path | `string` | yes | Resource type to export, such as media or text. |
| `mediaId` | path | `string` | yes | Speak Ai media or text identifier. |
| `fileType` | path | `string` | yes | Export format such as pdf, txt, docx, srt, or vtt. |
| `isSpeakerNames` | query | `boolean` | no | Whether speaker names should be included in the export. |
| `isTimeStamps` | query | `boolean` | no | Whether timestamps should be included in the export. |
| `isInsightVisualized` | query | `boolean` | no | Whether insights should be visualized in the export when supported. |
| `isRedacted` | query | `boolean` | no | Whether redacted content should be used in the export. |
