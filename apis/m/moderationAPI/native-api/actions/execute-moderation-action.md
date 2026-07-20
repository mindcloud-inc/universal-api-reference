# Execute Moderation Action with Moderation API

Executes a moderation action in Moderation API.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/execute`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Execute Moderation Action](https://docs.moderationapi.com/api-reference/actions/execute-moderation-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionKey` | body | `string` | yes | ID or key of the action to execute |
| `contentIds[]` | body | `array<string>` | no | IDs of the content items to apply the action to. Provide this or authorIds. |
| `authorIds[]` | body | `array<string>` | no | IDs of the authors to apply the action to. Provide this or contentIds. |
| `value` | body | `string` | no | Optional value to provide with the action |
| `queueId` | body | `string` | no | Optional queue ID if the action is queue-specific |
| `duration` | body | `number` | no | Optional duration in milliseconds for actions with timeouts |
