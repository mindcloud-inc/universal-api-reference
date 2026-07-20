# Get Glossary Term with Localazy

Retrieves a glossary term from a Localazy project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/glossary/:id`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Get Glossary Term](https://localazy.com/docs/api/glossary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id or slug. |
| `id` | path | `string` | yes | Glossary term identifier. |
