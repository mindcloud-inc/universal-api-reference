# Retell AI: Create Retell LLM

Creates a Retell LLM in Retell AI.

```
POST https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-retell-llm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-retell-llm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "generalTools[].type": "string",
  "generalTools[].name": "Ava Chen",
  "states[].name": "Ava Chen",
  "states[].edges[].destinationStateName": "Ava Chen",
  "states[].edges[].description": "string",
  "states[].edges[].parameters.type": "string",
  "states[].edges[].parameters.properties": {},
  "states[].tools[].type": "string",
  "states[].tools[].name": "Ava Chen",
  "mcps[].name": "Ava Chen",
  "mcps[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-retell-llm', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "generalTools[].type": "string",
    "generalTools[].name": "Ava Chen",
    "states[].name": "Ava Chen",
    "states[].edges[].destinationStateName": "Ava Chen",
    "states[].edges[].description": "string",
    "states[].edges[].parameters.type": "string",
    "states[].edges[].parameters.properties": {},
    "states[].tools[].type": "string",
    "states[].tools[].name": "Ava Chen",
    "mcps[].name": "Ava Chen",
    "mcps[].url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `generalTools[]` | array<object> | no | A list of tools the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use. - Tools of LLM (with state) = general tools + state tools + state transitions - Tools of LLM (no state) = general tools |
| `knowledgeBaseIds[]` | array<string> | no | A list of knowledge base ids to use for this resource. |
| `mcps[]` | array<object> | no | A list of MCPs to use for this LLM. |
| `model` | string | no | Available LLM models for agents. |
| `states[]` | array<object> | no | States of the LLM. This is to help reduce prompt length and tool choices when the call can be broken into distinct states. With shorter prompts and less tools, the LLM can better focus and follow the rules, minimizing hallucination. If this field is not set, the agent would only have general prompt and general tools (essentially one state). |
| `states[].edges[]` | array<object> | no | Edges of the state define how and what state can be reached from this state. |
| `states[].edges[].parameters.required[]` | array<string> | no | List of names of required property when generating this parameter. LLM will do its best to generate the required properties in its function arguments. Property must exist in properties. |
| `states[].tools[]` | array<object> | no | A list of tools specific to this state the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use. - Tools of LLM = general tools + state tools + state transitions |
| `s2sModel` | string | no | Select the underlying speech to speech model. Can only set this or model, not both. Allowed values: gpt-4o-realtime, gpt-4o-mini-realtime, gpt-realtime, gpt-realtime-mini. |
| `modelTemperature` | number | no | If set, will control the randomness of the response. Value ranging from [0,1]. Lower value means more deterministic, while higher value means more random. If unset, default value 0 will apply. Note that for tool calling, a lower value is recommended. |
| `modelHighPriority` | boolean | no | If set to true, will use high priority pool with more dedicated resource to ensure lower and more consistent latency, default to false. This feature usually comes with a higher cost. |
| `toolCallStrictMode` | boolean | no | Whether to use strict mode for tool calls. Only applicable when using certain supported models. |
| `knowledgeBaseIds[]` | array<string> | no | A list of knowledge base ids to use for this resource. |
| `knowledgeBaseIds[]` | array<string> | no | A list of knowledge base ids to use for this resource. |
| `kbConfig` | object | no |  |
| `kbConfig.topK` | number | no | Max number of knowledge base chunks to retrieve |
| `kbConfig.filterScore` | number | no | Similarity threshold for filtering search results |
| `startSpeaker` | string | no | The speaker who starts the conversation. Required. Must be either 'user' or 'agent'. Allowed values: user, agent. |
| `beginAfterUserSilenceMs` | number | no | If set, the AI will begin the conversation after waiting for the user for the duration (in milliseconds) specified by this attribute. This only applies if the agent is configured to wait for the user to speak first. If not set, the agent will wait indefinitely for the user to speak. |
| `beginMessage` | string | no | First utterance said by the agent in the call. If not set, LLM will dynamically generate a message. If set to "", agent will wait for user to speak first. |
| `generalPrompt` | string | no | General prompt appended to system prompt no matter what state the agent is in. - System prompt (with state) = general prompt + state prompt. - System prompt (no state) = general prompt. |
| `generalTools[]` | array<object> | no | A list of tools the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use. - Tools of LLM (with state) = general tools + state tools + state transitions - Tools of LLM (no state) = general tools |
| `generalTools[]` | array<object> | no | A list of tools the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use. - Tools of LLM (with state) = general tools + state tools + state transitions - Tools of LLM (no state) = general tools |
| `generalTools[].type` | string | yes | Allowed values: end_call. |
| `generalTools[].name` | string | yes | Name of the tool. Must be unique within all tools available to LLM at any given time (general tools + state tools + state transitions). Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `generalTools[].description` | string | no | Describes what the tool does, sometimes can also include information about when to call the tool. |
| `generalTools[].speakDuringExecution` | boolean | no | If true, will speak during execution. |
| `generalTools[].executionMessageDescription` | string | no | Describes what to say to user when ending the call. Only applicable when speak_during_execution is true. |
| `generalTools[].executionMessageType` | string | no | Type of execution message. "prompt" means the agent will use execution_message_description as a prompt to generate the message. "static_text" means the agent will speak the execution_message_description directly. Defaults to "prompt". Allowed values: prompt, static_text. |
| `states[]` | array<object> | no | States of the LLM. This is to help reduce prompt length and tool choices when the call can be broken into distinct states. With shorter prompts and less tools, the LLM can better focus and follow the rules, minimizing hallucination. If this field is not set, the agent would only have general prompt and general tools (essentially one state). |
| `states[]` | array<object> | no | States of the LLM. This is to help reduce prompt length and tool choices when the call can be broken into distinct states. With shorter prompts and less tools, the LLM can better focus and follow the rules, minimizing hallucination. If this field is not set, the agent would only have general prompt and general tools (essentially one state). |
| `states[].name` | string | yes | Name of the state, must be unique for each state. Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `states[].statePrompt` | string | no | Prompt of the state, will be appended to the system prompt of LLM. - System prompt = general prompt + state prompt. |
| `states[].edges[]` | array<object> | no | Edges of the state define how and what state can be reached from this state. |
| `states[].edges[]` | array<object> | no | Edges of the state define how and what state can be reached from this state. |
| `states[].edges[].destinationStateName` | string | yes | The destination state name when going through transition of state via this edge. State transition internally is implemented as a tool call of LLM, and a tool call with name "transition_to_{destination_state_name}" will get created. Feel free to reference it inside the prompt. |
| `states[].edges[].description` | string | yes | Describes what's the transition and at what time / criteria should this transition happen. |
| `states[].edges[].parameters` | object | no | The parameters the functions accepts, described as a JSON Schema object. See [JSON Schema reference](https://json-schema.org/understanding-json-schema/) for documentation about the format. Omitting parameters defines a function with an empty parameter list. |
| `states[].edges[].parameters.type` | string | yes | Type must be "object" for a JSON Schema object. Allowed values: object. |
| `states[].edges[].parameters.properties` | object | yes | The value of properties is an object, where each key is the name of a property and each value is a schema used to validate that property. |
| `states[].edges[].parameters.required[]` | array<string> | no | List of names of required property when generating this parameter. LLM will do its best to generate the required properties in its function arguments. Property must exist in properties. |
| `states[].edges[].parameters.required[]` | array<string> | no | List of names of required property when generating this parameter. LLM will do its best to generate the required properties in its function arguments. Property must exist in properties. |
| `states[].tools[]` | array<object> | no | A list of tools specific to this state the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use. - Tools of LLM = general tools + state tools + state transitions |
| `states[].tools[]` | array<object> | no | A list of tools specific to this state the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use. - Tools of LLM = general tools + state tools + state transitions |
| `states[].tools[].type` | string | yes | Allowed values: end_call. |
| `states[].tools[].name` | string | yes | Name of the tool. Must be unique within all tools available to LLM at any given time (general tools + state tools + state transitions). Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `states[].tools[].description` | string | no | Describes what the tool does, sometimes can also include information about when to call the tool. |
| `states[].tools[].speakDuringExecution` | boolean | no | If true, will speak during execution. |
| `states[].tools[].executionMessageDescription` | string | no | Describes what to say to user when ending the call. Only applicable when speak_during_execution is true. |
| `states[].tools[].executionMessageType` | string | no | Type of execution message. "prompt" means the agent will use execution_message_description as a prompt to generate the message. "static_text" means the agent will speak the execution_message_description directly. Defaults to "prompt". Allowed values: prompt, static_text. |
| `startingState` | string | no | Name of the starting state. Required if states is not empty. |
| `defaultDynamicVariables` | object | no | Default dynamic variables represented as key-value pairs of strings. These are injected into your Retell LLM prompt and tool description when specific values are not provided in a request. Only applicable for Retell LLM. |
| `version` | number | no | The version of the LLM. |
| `mcps[]` | array<object> | no | A list of MCPs to use for this LLM. |
| `mcps[]` | array<object> | no | A list of MCPs to use for this LLM. |
| `mcps[].name` | string | yes |  |
| `mcps[].url` | string | yes | The URL of the MCP server. |
| `mcps[].headers` | object | no | Headers to add to the MCP connection request. |
| `mcps[].queryParams` | object | no | Query parameters to append to the MCP connection request URL. |
| `mcps[].timeoutMs` | number | no | Maximum time to wait for a connection to be established (in milliseconds). Default to 120,000 ms (2 minutes). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "beginAfterUserSilenceMs": 1,
      "beginMessage": "string",
      "defaultDynamicVariables": {},
      "generalPrompt": "string",
      "generalTools": [
        {
          "description": "string",
          "executionMessageDescription": "string",
          "executionMessageType": "string",
          "name": "Ava Chen",
          "speakDuringExecution": true,
          "type": "string"
        }
      ],
      "isPublished": true,
      "kbConfig": {
        "filterScore": 1,
        "topK": 1
      },
      "knowledgeBaseIds": [
        "string"
      ],
      "lastModificationTimestamp": 1,
      "llmId": "string",
      "mcps": [
        {
          "headers": {},
          "name": "Ava Chen",
          "queryParams": {},
          "timeoutMs": 1,
          "url": "https://example.com"
        }
      ],
      "model": "string",
      "modelHighPriority": true,
      "modelTemperature": 1,
      "s2sModel": "string",
      "startingState": "string",
      "startSpeaker": "string",
      "states": [
        {
          "edges": [
            {
              "description": "string",
              "destinationStateName": "Ava Chen",
              "parameters": {
                "properties": {},
                "required": [
                  "string"
                ],
                "type": "string"
              }
            }
          ],
          "name": "Ava Chen",
          "statePrompt": "string",
          "tools": [
            {
              "description": "string",
              "executionMessageDescription": "string",
              "executionMessageType": "string",
              "name": "Ava Chen",
              "speakDuringExecution": true,
              "type": "string"
            }
          ]
        }
      ],
      "toolCallStrictMode": true,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beginAfterUserSilenceMs` | number | If set, the AI will begin the conversation after waiting for the user for the duration (in milliseconds) specified by this attribute. This only applies if the agent is configured to wait for the user to speak first. If not set, the agent will wait indefinitely for the user to speak. |
| `beginMessage` | string | First utterance said by the agent in the call. If not set, LLM will dynamically generate a message. If set to "", agent will wait for user to speak first. |
| `defaultDynamicVariables` | object | Default dynamic variables represented as key-value pairs of strings. These are injected into your Retell LLM prompt and tool description when specific values are not provided in a request. Only applicable for Retell LLM. |
| `generalPrompt` | string | General prompt appended to system prompt no matter what state the agent is in.  - System prompt (with state) = general prompt + state prompt. - System prompt (no state) = general prompt. |
| `generalTools` | array<object> | A list of tools the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM (with state) = general tools + state tools + state transitions - Tools of LLM (no state) = general tools |
| `generalTools[].description` | string | Describes what the tool does, sometimes can also include information about when to call the tool. |
| `generalTools[].executionMessageDescription` | string | Describes what to say to user when ending the call. Only applicable when speak_during_execution is true. |
| `generalTools[].executionMessageType` | string | Type of execution message. "prompt" means the agent will use execution_message_description as a prompt to generate the message. "static_text" means the agent will speak the execution_message_description directly. Defaults to "prompt". Allowed values: prompt, static_text. |
| `generalTools[].name` | string | Name of the tool. Must be unique within all tools available to LLM at any given time (general tools + state tools + state transitions). Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `generalTools[].speakDuringExecution` | boolean | If true, will speak during execution. |
| `generalTools[].type` | string | Allowed values: end_call. |
| `isPublished` | boolean | Whether the Retell LLM Response Engine is published. |
| `kbConfig` | object |  |
| `kbConfig.filterScore` | number | Similarity threshold for filtering search results |
| `kbConfig.topK` | number | Max number of knowledge base chunks to retrieve |
| `knowledgeBaseIds` | array<string> | A list of knowledge base ids to use for this resource. |
| `lastModificationTimestamp` | number | Last modification timestamp (milliseconds since epoch). Either the time of last update or creation if no updates available. |
| `llmId` | string | Unique id of Retell LLM Response Engine. |
| `mcps` | array<object> | A list of MCPs to use for this LLM. |
| `mcps[].headers` | object | Headers to add to the MCP connection request. |
| `mcps[].name` | string |  |
| `mcps[].queryParams` | object | Query parameters to append to the  MCP connection request URL. |
| `mcps[].timeoutMs` | number | Maximum time to wait for a connection to be established (in milliseconds). Default to 120,000 ms (2 minutes). |
| `mcps[].url` | string | The URL of the MCP server. |
| `model` | string | Available LLM models for agents. |
| `modelHighPriority` | boolean | If set to true, will use high priority pool with more dedicated resource to ensure lower and more consistent latency, default to false. This feature usually comes with a higher cost. |
| `modelTemperature` | number | If set, will control the randomness of the response. Value ranging from [0,1]. Lower value means more deterministic, while higher value means more random. If unset, default value 0 will apply. Note that for tool calling, a lower value is recommended. |
| `s2sModel` | string | Select the underlying speech to speech model. Can only set this or model, not both. Allowed values: gpt-4o-realtime, gpt-4o-mini-realtime, gpt-realtime, gpt-realtime-mini. |
| `startingState` | string | Name of the starting state. Required if states is not empty. |
| `startSpeaker` | string | The speaker who starts the conversation. Required. Must be either 'user' or 'agent'. Allowed values: user, agent. |
| `states` | array<object> | States of the LLM. This is to help reduce prompt length and tool choices when the call can be broken into distinct states. With shorter prompts and less tools, the LLM can better focus and follow the rules, minimizing hallucination. If this field is not set, the agent would only have general prompt and general tools (essentially one state). |
| `states[].edges` | array<object> | Edges of the state define how and what state can be reached from this state. |
| `states[].edges[].description` | string | Describes what's the transition and at what time / criteria should this transition happen. |
| `states[].edges[].destinationStateName` | string | The destination state name when going through transition of state via this edge. State transition internally is implemented as a tool call of LLM, and a tool call with name "transition_to_{destination_state_name}" will get created. Feel free to reference it inside the prompt. |
| `states[].edges[].parameters` | object | The parameters the functions accepts, described as a JSON Schema object. See [JSON Schema reference](https://json-schema.org/understanding-json-schema/) for documentation about the format. Omitting parameters defines a function with an empty parameter list. |
| `states[].edges[].parameters.properties` | object | The value of properties is an object, where each key is the name of a property and each value is a schema used to validate that property. |
| `states[].edges[].parameters.required` | array<string> | List of names of required property when generating this parameter. LLM will do its best to generate the required properties in its function arguments. Property must exist in properties. |
| `states[].edges[].parameters.type` | string | Type must be "object" for a JSON Schema object. Allowed values: object. |
| `states[].name` | string | Name of the state, must be unique for each state. Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `states[].statePrompt` | string | Prompt of the state, will be appended to the system prompt of LLM.  - System prompt = general prompt + state prompt. |
| `states[].tools` | array<object> | A list of tools specific to this state the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM = general tools + state tools + state transitions |
| `states[].tools[].description` | string | Describes what the tool does, sometimes can also include information about when to call the tool. |
| `states[].tools[].executionMessageDescription` | string | Describes what to say to user when ending the call. Only applicable when speak_during_execution is true. |
| `states[].tools[].executionMessageType` | string | Type of execution message. "prompt" means the agent will use execution_message_description as a prompt to generate the message. "static_text" means the agent will speak the execution_message_description directly. Defaults to "prompt". Allowed values: prompt, static_text. |
| `states[].tools[].name` | string | Name of the tool. Must be unique within all tools available to LLM at any given time (general tools + state tools + state transitions). Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `states[].tools[].speakDuringExecution` | boolean | If true, will speak during execution. |
| `states[].tools[].type` | string | Allowed values: end_call. |
| `toolCallStrictMode` | boolean | Whether to use strict mode for tool calls. Only applicable when using certain supported models. |
| `version` | number | The version of the LLM. |

## Native endpoint

Through the native Retell AI API, this operation is `POST /create-retell-llm` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-retell-llm.md) for the provider-specific parameters and requirements.

