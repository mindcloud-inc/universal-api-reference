# Archive or Unarchive Project by ID with Filestage

Archives or unarchives a Filestage project by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{projectId}/isArchived`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Archive or Unarchive Project by ID](https://developers.filestage.io/docs/api/riodpev6z6775-archive-unarchive-project-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project Id |
| `isArchived` | body | `boolean` | yes | — |
