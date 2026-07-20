# Revoke Task with MoreApp

Revokes a task in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/customers/{{customerId}}/{{formId}}/tasks/{{taskId}}/revoke`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Revoke Task](https://docs.moreapp.com/docs/developer-docs/41a7f9dc561ff-revoke-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `formId` | path | `string` | yes | MoreApp form identifier. |
| `taskId` | path | `string` | yes | MoreApp task identifier. |
