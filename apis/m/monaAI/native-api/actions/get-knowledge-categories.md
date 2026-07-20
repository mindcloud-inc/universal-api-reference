# Get Knowledge Categories with Mona AI

Retrieves knowledge categories from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/companyKnowledge/getCategories`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Knowledge Categories](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeCount` | body | `boolean` | no | Whether to include category item counts. |
| `includeEmpty` | body | `boolean` | no | Whether to include empty categories. |
| `permission` | body | `string` | yes | Mona permission string required by the categories endpoint. |
