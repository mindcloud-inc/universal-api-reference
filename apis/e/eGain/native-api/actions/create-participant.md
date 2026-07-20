# Create Participant with eGain

Creates a new participant in eGain.

## Endpoint

- **Method:** `POST`
- **Path:** `/participants`
- **Base URL:** `https://api.ai.egain.cloud/conversation/conversationmgr/v3`
- **Official documentation:** [Create Participant](https://apidev.egain.com/apis/v3/conversation/conversationmgr/api-bundled/participant/createparticipant.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Whether the participant is active. |
| `application.id` | body | `string` | yes | Client application ID. |
| `name` | body | `string` | yes | Participant name. |
| `type` | body | `string` | yes | Participant type. |
