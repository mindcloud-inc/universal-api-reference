# Issue Credentials with Digit.ink

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials`
- **Base URL:** `https://app.digit.ink/api/v1`
- **Official documentation:** [Issue Credentials](https://app.digit.ink/api/v1/classic-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productKey` | body | `list` | yes | Digit.ink product key. Accepted values: `BLOCKCHAIN_CREDENTIALS`, `DIGITAL_CREDENTIALS`, `RECIPIENTS`. |
| `templateUuid` | body | `string` | yes | Template UUID for credential issuance. |
| `csvString` | body | `string` | yes | CSV string containing credential recipients. |
| `credentialTitle` | body | `string` | no | Optional credential title override. |
| `description` | body | `string` | no | Optional credential description override. |
| `lmsData` | body | `string` | no | Optional LMS data payload string. |
| `isTestRun` | body | `boolean` | no | Whether to run the issue request as a test. |
