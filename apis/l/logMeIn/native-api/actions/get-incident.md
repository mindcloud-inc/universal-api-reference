# Get Incident with LogMeIn

Retrieves an existing incident from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/goto-resolve-ticketing/v1/incidents/:referenceNum`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Get Incident](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceNum` | path | `string` | yes | Required incident reference number. |
| `include` | query | `string` | no | Related entities to include. |
| `extraFields` | query | `string` | no | Extra fields to include. |
