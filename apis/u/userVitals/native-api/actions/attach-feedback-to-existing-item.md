# Attach Feedback To Existing Item with UserVitals

Attaches feedback to an existing idea or story.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback/attach`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Attach Feedback To Existing Item](https://api.roadmap.space/#attach-to-existing-idea-or-story)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentId` | body | `string` | yes | The target idea or story id. |
| `parentToken` | body | `string` | yes | The target idea or story token. |
| `sourceId` | body | `string` | yes | The feedback id to attach. |
| `sourceToken` | body | `string` | yes | The feedback token to attach. |
