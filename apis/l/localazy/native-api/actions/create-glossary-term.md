# Create Glossary Term with Localazy

Creates a new glossary term in a Localazy project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/glossary`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Create Glossary Term](https://localazy.com/docs/api/glossary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id or slug. |
| `description` | body | `string` | no | Glossary term description. |
| `translateTerm` | body | `boolean` | no | Whether Localazy should translate the term. |
| `caseSensitive` | body | `boolean` | no | Whether the term match is case-sensitive. |
| `exactMatch` | body | `boolean` | no | Whether Localazy should match the whole term exactly. |
| `term[]` | body | `array<object>` | yes | Source term plus translations. |
| `term[].lang` | body | `string` | yes | Language code for the glossary value. |
| `term[].term` | body | `string` | yes | Glossary value in the selected language. |
