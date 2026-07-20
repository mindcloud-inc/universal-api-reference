# Delete Glossary Term with Localazy

Deletes an existing glossary term from a Localazy project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/glossary/:id`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Delete Glossary Term](https://localazy.com/docs/api/glossary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id or slug. |
| `id` | path | `string` | yes | Glossary term identifier. |
