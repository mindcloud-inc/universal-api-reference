# List Stacks with Digit.ink

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks`
- **Base URL:** `https://app.digit.ink/api/v1`
- **Official documentation:** [List Stacks](https://app.digit.ink/api/v1/classic-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `list` | yes | Digit.ink stack filter key. Accepted values: `issued`, `stackName`, `stackUuid`. |
| `value` | query | `string` | yes | Digit.ink stack filter value. |
