# Rename Project by ID with Filestage

Updates a Filestage project name by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{projectId}/name`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Rename Project by ID](https://developers.filestage.io/docs/api/huaimmzpi8uib-rename-project-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project Id |
| `name` | body | `string` | yes | — |
