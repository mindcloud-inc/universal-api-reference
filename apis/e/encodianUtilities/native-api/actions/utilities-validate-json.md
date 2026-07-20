# Utilities - Validate JSON with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ValidateJson`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Validate JSON](https://support.encodian.com/hc/en-gb/articles/12722049993500)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `json` | body | `string` | yes | The JSON data to validate |
| `schema` | body | `string` | no | Optional - A JSON schema to apply to the validation |
