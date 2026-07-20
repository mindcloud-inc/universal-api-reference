# Retell AI: Get Retell LLM

Retrieves a Retell LLM from Retell AI.

```
GET https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/get-retell-llm
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/get-retell-llm?connectionId=$CONNECTION_ID&llmId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "llmId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/get-retell-llm?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `llmId` | string | yes |  |
| `version` | number | no |  |

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

Through the native Retell AI API, this operation is `GET /get-retell-llm/{llm_id}` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-retell-llm.md) for the provider-specific parameters and requirements.

