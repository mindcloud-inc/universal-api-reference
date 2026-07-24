# List Payment Audit Logs with Rillion Prime Pay

## Endpoint

- **Method:** `GET`
- **Path:** `/payment/audit`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Payment Audit Logs](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Pay%20-%20v1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchReferenceId` | query | `string` | yes | Reference ID to search for in payment audit logs. |
| `referenceType` | query | `list<string>` | yes | Reference type to search for in payment audit logs. |
