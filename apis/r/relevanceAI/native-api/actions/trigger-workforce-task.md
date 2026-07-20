# Trigger Workforce Task with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/workforce/trigger`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Trigger Workforce Task](https://relevanceai.com/docs/build/workforces/workforce-features/workforce-task-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trigger.message.role` | body | `string` | no | The role for the trigger message. Defaults to user. |
| `workforce_id` | body | `string` | yes | The workforce id to trigger. |
| `trigger.message.content` | body | `string` | yes | The user message to send to the workforce. |
