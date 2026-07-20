# List Credentials with Digit.ink

## Endpoint

- **Method:** `GET`
- **Path:** `/credentials`
- **Base URL:** `https://app.digit.ink/api/v1`
- **Official documentation:** [List Credentials](https://app.digit.ink/api/v1/classic-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `list` | yes | Digit.ink credential filter key. Accepted values: `credentialTitle`, `credentialUuid`, `email`, `issued`, `name`, `templateName`, `templateUuid`. |
| `value` | query | `string` | yes | Digit.ink credential filter value. |
