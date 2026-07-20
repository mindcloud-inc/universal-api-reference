# Generate Test Signature with Currents

## Endpoint

- **Method:** `POST`
- **Path:** `/signature/test`
- **Base URL:** `https://api.currents.dev/v1`
- **Official documentation:** [Generate Test Signature](https://docs.currents.dev/resources/api/api-resources/test-signature)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | body | `string` | yes |
| `specFilePath` | body | `string` | yes |
| `testTitle` | body | `string` | yes |
