# List Batches with Digit.ink

## Endpoint

- **Method:** `GET`
- **Path:** `/batches`
- **Base URL:** `https://app.digit.ink/api/v1`
- **Official documentation:** [List Batches](https://app.digit.ink/api/v1/classic-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `list` | yes | Digit.ink batch filter key. Accepted values: `batchUuid`, `credentialTitle`, `issued`, `ltiData`, `templateName`, `templateUuid`. |
| `value` | query | `string` | yes | Digit.ink batch filter value. |
