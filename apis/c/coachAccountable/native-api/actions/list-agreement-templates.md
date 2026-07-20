# List Agreement Templates with CoachAccountable

Retrieves agreement templates from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Agreement Templates](https://www.coachaccountable.com/APIDocs#Agreement.getTemplates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Filter Agreement Templates by which title, prefixed. |
| `includeContent` | body | `boolean` | no | Set to true to include the full HTML content of the Agreement Templates. |
