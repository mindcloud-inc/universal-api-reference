# Show Rule with SonarQube

Retrieves a rule from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/rules/show`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Show Rule](https://sonarcloud.io/web_api/api/rules/show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `string` | yes | Rule key. Required by /api/rules/show. |
| `organization` | query | `string` | yes | SonarCloud organization key. Required by /api/rules/show. |
