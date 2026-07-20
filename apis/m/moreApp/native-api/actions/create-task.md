# Create Task with MoreApp

Creates a task in MoreApp.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.0/customers/{{customerId}}/{{formId}}/tasks`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Create Task](https://docs.moreapp.com/docs/developer-docs/657b678d8ad54-create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `data` | body | `object` | yes | Form data payload for the task. |
| `formId` | path | `string` | yes | MoreApp form identifier. |
| `message` | body | `string` | yes | Task message. |
| `publishInfo` | body | `object` | yes | Task publish scheduling object. |
| `recipients[]` | body | `array<string>` | yes | Email recipients for the task. Send multiple values as a array. |
