# Update Dialogflow Agent with SignalWire

Updates an existing Dialogflow agent in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/dialogflow_agents/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update Dialogflow Agent](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-dialogflow/update-dialogflow-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a Dialogflow Agent. |
| `name` | body | `string` | no | Name of the Dialogflow Agent |
| `say_enabled` | body | `boolean` | no | Whether to enable the 'say' feature |
| `say` | body | `string` | no | Default message to say |
| `voice` | body | `string` | no | Voice to use for speech |
