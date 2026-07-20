# Interact Non-Stream with Voiceflow

Sends a conversation action to Voiceflow and returns traces.

## Endpoint

- **Method:** `POST`
- **Path:** `/state/user/:userId/interact`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Interact Non-Stream](https://docs.voiceflow.com/api-reference/conversation/interact-non-stream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | An ID which uniquely identifies the user having the conversation. |
| `state` | body | `object` | no | Optional conversation state payload. |
| `request` | body | `object` | no | The user's request payload. |
| `action` | body | `object` | no | The action payload used to launch or control the interaction. |
| `config` | body | `object` | no | Optional settings to configure the response. |
