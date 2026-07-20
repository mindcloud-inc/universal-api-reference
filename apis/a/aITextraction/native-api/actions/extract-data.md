# Extract Data with AI Textraction

Extracts user-defined entities from unstructured text with AI Textraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/textraction`
- **Base URL:** `https://ai-textraction.p.rapidapi.com`
- **Official documentation:** [Extract Data](https://rapidapi.com/textractionai/api/ai-textraction/details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The free-form text to extract data from. |
| `entities` | body | `object<object>` | yes | A JSON array of entity definitions. Each item should include var_name, type, and description. |
