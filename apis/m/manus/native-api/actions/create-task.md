# Create Task with Manus

Creates a new task in Manus.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.manus.ai/v1`
- **Official documentation:** [Create Task](https://open.manus.ai/docs/v1/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | The task prompt or instruction for the Manus agent |
| `agentProfile` | body | `string` | yes | The Manus model profile to use |
| `taskMode` | body | `string` | no | Task mode: chat, adaptive, or agent |
| `hideInTaskList` | body | `boolean` | no | Hide the task from the Manus web app task list |
| `createShareableLink` | body | `boolean` | no | Make the chat publicly accessible |
| `taskId` | body | `string` | no | Continue an existing task |
| `locale` | body | `string` | no | Locale such as en-US |
| `interactiveMode` | body | `boolean` | no | Allow Manus to ask follow-up questions |
