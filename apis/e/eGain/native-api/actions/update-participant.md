# Update Participant with eGain

Updates an existing participant in eGain.

## Endpoint

- **Method:** `PUT`
- **Path:** `/participants/:id`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Update Participant](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/participant/updateparticipant.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether participant is active. |
| `application.id` | body | `string` | yes | Client application ID. |
| `id` | path | `string` | yes | Participant ID. |
| `name` | body | `string` | yes | Participant name. |
| `type` | body | `string` | yes | Participant type. |
