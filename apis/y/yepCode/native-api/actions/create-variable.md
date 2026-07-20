# Create variable with YepCode

Creates a new variable in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/variables`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Create variable](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Variables/createVariable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | no | Variable key or name. |
| `value` | body | `string` | no | Variable value. |
| `isSensitive` | body | `boolean` | no | Whether the variable value should be treated as sensitive. |
