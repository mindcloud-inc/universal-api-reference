# Create Project Participants with Morningmate

Adds participants to a Morningmate project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/[:projectId]/participants`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Create Project Participants](https://api.morningmate.com/docs/api/v1/projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Morningmate numeric project ID |
| `registerId` | body | `string` | yes | Morningmate author user ID |
| `participants[]` | body | `array<object>` | yes | Participants array |
| `participants[].participantId` | body | `string` | yes | Participant ID to add |
