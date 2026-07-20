# List Payment Audit Logs with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/audit`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Payment Audit Logs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchReferenceId` | query | `string` | yes | Optional query value for SearchReferenceId. |
| `referenceType` | query | `string` | yes | Optional query value for ReferenceType. |
