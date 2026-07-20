# Get Approver Type with Damstra Forms

Retrieves an approver type from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/approver_types/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Approver Type](https://sammapi.docs.apiary.io/#reference/approver-types/approver-type-instance/get-an-approver-type)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the approver type. |
| `show_managed` | query | `boolean` | no | Show/hide the managed attribute. |
