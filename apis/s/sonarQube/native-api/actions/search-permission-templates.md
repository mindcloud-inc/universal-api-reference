# Search Permission Templates with SonarQube

Finds permission templates in SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/permissions/search_templates`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Search Permission Templates](https://sonarcloud.io/web_api/api/permissions/search_templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `string` | yes | Organization key. Required by /api/permissions/search_templates. |
