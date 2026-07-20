# Update An Action with Moderation API

Updates a moderation action in Moderation API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/actions/:id`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Update An Action](https://docs.moderationapi.com/api-reference/actions/update-an-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the action to update. |
| `key` | body | `string` | no | User defined key of the action. |
| `name` | body | `string` | no | The name of the action. |
| `description` | body | `string` | no | The description of the action. |
| `type` | body | `string` | no | The type of the action. |
| `builtIn` | body | `boolean` | no | Whether the action is a built-in action or a custom one. |
| `queueBehaviour` | body | `string` | no | Whether the action resolves and removes the item, unresolves and re-add it to the queue, or does not change the resolve status. |
| `filterInQueueIds[]` | body | `array<string>` | no | The IDs of the queues the action is available in. |
| `position` | body | `string` | no | Show the action in all queues, selected queues or no queues (to use via API only). |
| `possibleValues[]` | body | `array<object>` | no | The possible values of the action. The user will be prompted to select one of these values when executing the action. |
| `valueRequired` | body | `boolean` | no | Whether the action requires a value to be executed. |
| `freeText` | body | `boolean` | no | Whether the action allows any text to be entered as a value or if it must be one of the possible values. |
