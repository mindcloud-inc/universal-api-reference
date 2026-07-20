# Validate Agent Configuration with SVAHNAR

Validates an agent configuration in SVAHNAR.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/validate`
- **Base URL:** `https://api.svahnar.com`
- **Official documentation:** [Validate Agent Configuration](https://docs.svahnar.com/docs/Agents/validate_config/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `yaml_string` | body | `string` | yes | YAML string to validate. |
