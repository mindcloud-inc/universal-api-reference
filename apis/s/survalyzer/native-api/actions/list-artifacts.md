# List Artifacts with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Common/v3/ReadArtifactList`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [List Artifacts](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | Artifact folder path to list, for example Images. |
| `workspaceId` | body | `number` | no | Workspace identifier to search for artifacts. |
