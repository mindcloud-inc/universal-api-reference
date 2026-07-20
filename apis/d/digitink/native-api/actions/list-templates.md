# List Templates with Digit.ink

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://app.digit.ink/api/v1`
- **Official documentation:** [List Templates](https://app.digit.ink/api/v1/classic-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `list` | yes | Digit.ink template filter key. Accepted values: `credentialType`, `name`, `templateUuid`. |
| `value` | query | `string` | yes | Digit.ink template filter value. |
