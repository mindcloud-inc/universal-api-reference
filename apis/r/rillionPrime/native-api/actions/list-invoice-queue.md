# List Invoice Queue with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/invoicequeue/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Invoice Queue](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=Invoice%20-%20v1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | path | `string` | yes | Path value for Role. |
| `headersOnly` | query | `boolean` | no | When true, returns only header rows where supported. |
| `updateQueueStatus` | query | `boolean` | no | Optional query value for UpdateQueueStatus. |
| `searchTerm` | query | `string` | no | Optional query value for SearchTerm. |
