# Create Retell LLM with Retell AI

Creates a Retell LLM in Retell AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-retell-llm`
- **Base URL:** `https://api.retellai.com`
- **Official documentation:** [Create Retell LLM](https://docs.retellai.com/api-references/create-retell-llm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `general_tools[]` | body | `array<object>` | no | A list of tools the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM (with state) = general tools + state tools + state transitions - Tools of LLM (no state) = general tools |
| `knowledge_base_ids[]` | body | `array<string>` | no | A list of knowledge base ids to use for this resource. |
| `mcps[]` | body | `array<object>` | no | A list of MCPs to use for this LLM. |
| `model` | body | `string` | no | Available LLM models for agents. |
| `states[]` | body | `array<object>` | no | States of the LLM. This is to help reduce prompt length and tool choices when the call can be broken into distinct states. With shorter prompts and less tools, the LLM can better focus and follow the rules, minimizing hallucination. If this field is not set, the agent would only have general prompt and general tools (essentially one state). |
| `states[].edges[]` | body | `array<object>` | no | Edges of the state define how and what state can be reached from this state. |
| `states[].edges[].parameters.required[]` | body | `array<string>` | no | List of names of required property when generating this parameter. LLM will do its best to generate the required properties in its function arguments. Property must exist in properties. |
| `states[].tools[]` | body | `array<object>` | no | A list of tools specific to this state the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM = general tools + state tools + state transitions |
| `s2s_model` | body | `string` | no | Select the underlying speech to speech model. Can only set this or model, not both. Allowed values: gpt-4o-realtime, gpt-4o-mini-realtime, gpt-realtime, gpt-realtime-mini. |
| `model_temperature` | body | `number` | no | If set, will control the randomness of the response. Value ranging from [0,1]. Lower value means more deterministic, while higher value means more random. If unset, default value 0 will apply. Note that for tool calling, a lower value is recommended. |
| `model_high_priority` | body | `boolean` | no | If set to true, will use high priority pool with more dedicated resource to ensure lower and more consistent latency, default to false. This feature usually comes with a higher cost. |
| `tool_call_strict_mode` | body | `boolean` | no | Whether to use strict mode for tool calls. Only applicable when using certain supported models. |
| `knowledge_base_ids[]` | body | `array<string>` | no | A list of knowledge base ids to use for this resource. |
| `knowledge_base_ids[]` | body | `array<string>` | no | A list of knowledge base ids to use for this resource. |
| `kb_config` | body | `object` | no | — |
| `kb_config.top_k` | body | `number` | no | Max number of knowledge base chunks to retrieve |
| `kb_config.filter_score` | body | `number` | no | Similarity threshold for filtering search results |
| `start_speaker` | body | `string` | no | The speaker who starts the conversation. Required. Must be either 'user' or 'agent'. Allowed values: user, agent. |
| `begin_after_user_silence_ms` | body | `number` | no | If set, the AI will begin the conversation after waiting for the user for the duration (in milliseconds) specified by this attribute. This only applies if the agent is configured to wait for the user to speak first. If not set, the agent will wait indefinitely for the user to speak. |
| `begin_message` | body | `string` | no | First utterance said by the agent in the call. If not set, LLM will dynamically generate a message. If set to "", agent will wait for user to speak first. |
| `general_prompt` | body | `string` | no | General prompt appended to system prompt no matter what state the agent is in.  - System prompt (with state) = general prompt + state prompt. - System prompt (no state) = general prompt. |
| `general_tools[]` | body | `array<object>` | no | A list of tools the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM (with state) = general tools + state tools + state transitions - Tools of LLM (no state) = general tools |
| `general_tools[]` | body | `array<object>` | no | A list of tools the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM (with state) = general tools + state tools + state transitions - Tools of LLM (no state) = general tools |
| `general_tools[].type` | body | `string` | yes | Allowed values: end_call. |
| `general_tools[].name` | body | `string` | yes | Name of the tool. Must be unique within all tools available to LLM at any given time (general tools + state tools + state transitions). Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `general_tools[].description` | body | `string` | no | Describes what the tool does, sometimes can also include information about when to call the tool. |
| `general_tools[].speak_during_execution` | body | `boolean` | no | If true, will speak during execution. |
| `general_tools[].execution_message_description` | body | `string` | no | Describes what to say to user when ending the call. Only applicable when speak_during_execution is true. |
| `general_tools[].execution_message_type` | body | `string` | no | Type of execution message. "prompt" means the agent will use execution_message_description as a prompt to generate the message. "static_text" means the agent will speak the execution_message_description directly. Defaults to "prompt". Allowed values: prompt, static_text. |
| `states[]` | body | `array<object>` | no | States of the LLM. This is to help reduce prompt length and tool choices when the call can be broken into distinct states. With shorter prompts and less tools, the LLM can better focus and follow the rules, minimizing hallucination. If this field is not set, the agent would only have general prompt and general tools (essentially one state). |
| `states[]` | body | `array<object>` | no | States of the LLM. This is to help reduce prompt length and tool choices when the call can be broken into distinct states. With shorter prompts and less tools, the LLM can better focus and follow the rules, minimizing hallucination. If this field is not set, the agent would only have general prompt and general tools (essentially one state). |
| `states[].name` | body | `string` | yes | Name of the state, must be unique for each state. Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `states[].state_prompt` | body | `string` | no | Prompt of the state, will be appended to the system prompt of LLM.  - System prompt = general prompt + state prompt. |
| `states[].edges[]` | body | `array<object>` | no | Edges of the state define how and what state can be reached from this state. |
| `states[].edges[]` | body | `array<object>` | no | Edges of the state define how and what state can be reached from this state. |
| `states[].edges[].destination_state_name` | body | `string` | yes | The destination state name when going through transition of state via this edge. State transition internally is implemented as a tool call of LLM, and a tool call with name "transition_to_{destination_state_name}" will get created. Feel free to reference it inside the prompt. |
| `states[].edges[].description` | body | `string` | yes | Describes what's the transition and at what time / criteria should this transition happen. |
| `states[].edges[].parameters` | body | `object` | no | The parameters the functions accepts, described as a JSON Schema object. See [JSON Schema reference](https://json-schema.org/understanding-json-schema/) for documentation about the format. Omitting parameters defines a function with an empty parameter list. |
| `states[].edges[].parameters.type` | body | `string` | yes | Type must be "object" for a JSON Schema object. Allowed values: object. |
| `states[].edges[].parameters.properties` | body | `object` | yes | The value of properties is an object, where each key is the name of a property and each value is a schema used to validate that property. |
| `states[].edges[].parameters.required[]` | body | `array<string>` | no | List of names of required property when generating this parameter. LLM will do its best to generate the required properties in its function arguments. Property must exist in properties. |
| `states[].edges[].parameters.required[]` | body | `array<string>` | no | List of names of required property when generating this parameter. LLM will do its best to generate the required properties in its function arguments. Property must exist in properties. |
| `states[].tools[]` | body | `array<object>` | no | A list of tools specific to this state the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM = general tools + state tools + state transitions |
| `states[].tools[]` | body | `array<object>` | no | A list of tools specific to this state the model may call (to get external knowledge, call API, etc). You can select from some common predefined tools like end call, transfer call, etc; or you can create your own custom tool for the LLM to use.  - Tools of LLM = general tools + state tools + state transitions |
| `states[].tools[].type` | body | `string` | yes | Allowed values: end_call. |
| `states[].tools[].name` | body | `string` | yes | Name of the tool. Must be unique within all tools available to LLM at any given time (general tools + state tools + state transitions). Must be consisted of a-z, A-Z, 0-9, or contain underscores and dashes, with a maximum length of 64 (no space allowed). |
| `states[].tools[].description` | body | `string` | no | Describes what the tool does, sometimes can also include information about when to call the tool. |
| `states[].tools[].speak_during_execution` | body | `boolean` | no | If true, will speak during execution. |
| `states[].tools[].execution_message_description` | body | `string` | no | Describes what to say to user when ending the call. Only applicable when speak_during_execution is true. |
| `states[].tools[].execution_message_type` | body | `string` | no | Type of execution message. "prompt" means the agent will use execution_message_description as a prompt to generate the message. "static_text" means the agent will speak the execution_message_description directly. Defaults to "prompt". Allowed values: prompt, static_text. |
| `starting_state` | body | `string` | no | Name of the starting state. Required if states is not empty. |
| `default_dynamic_variables` | body | `object` | no | Default dynamic variables represented as key-value pairs of strings. These are injected into your Retell LLM prompt and tool description when specific values are not provided in a request. Only applicable for Retell LLM. |
| `version` | body | `number` | no | The version of the LLM. |
| `mcps[]` | body | `array<object>` | no | A list of MCPs to use for this LLM. |
| `mcps[]` | body | `array<object>` | no | A list of MCPs to use for this LLM. |
| `mcps[].name` | body | `string` | yes | — |
| `mcps[].url` | body | `string` | yes | The URL of the MCP server. |
| `mcps[].headers` | body | `object` | no | Headers to add to the MCP connection request. |
| `mcps[].query_params` | body | `object` | no | Query parameters to append to the  MCP connection request URL. |
| `mcps[].timeout_ms` | body | `number` | no | Maximum time to wait for a connection to be established (in milliseconds). Default to 120,000 ms (2 minutes). |
