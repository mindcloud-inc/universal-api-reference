# Update Glossary Term with Localazy

Updates an existing glossary term in a Localazy project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/glossary/:id`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Update Glossary Term](https://localazy.com/docs/api/glossary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id or slug. |
| `id` | path | `string` | yes | Glossary term identifier. |
| `description` | body | `string` | no | Glossary term description. |
| `translateTerm` | body | `boolean` | no | Whether Localazy should translate the term. |
| `caseSensitive` | body | `boolean` | no | Whether the term match is case-sensitive. |
| `exactMatch` | body | `boolean` | no | Whether Localazy should match the whole term exactly. |
| `term[]` | body | `array<object>` | yes | Source term plus translations. |
| `term[].lang` | body | `string` | yes | Language code for the glossary value. |
| `term[].term` | body | `string` | yes | Glossary value in the selected language. |
