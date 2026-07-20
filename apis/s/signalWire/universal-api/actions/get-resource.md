# SignalWire: Get Resource

Retrieves a resource from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-resource?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-resource?${params}`, {
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
| `id` | string | yes | Unique ID of a Resource. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_agent": {
        "agent_id": "string",
        "name": "Ava Chen",
        "params": {
          "acknowledge_interruptions": true,
          "ai_name": "Ava Chen",
          "ai_volume": 1,
          "app_name": "Ava Chen",
          "attention_timeout": 1,
          "attention_timeout_prompt": "string",
          "background_file": "string",
          "background_file_loops": 1,
          "background_file_volume": 1,
          "barge_match_string": "string",
          "barge_min_words": 1,
          "conscience": "string",
          "conversation_id": "string",
          "convo": [
            {}
          ],
          "debug": true,
          "debug_webhook_level": 1,
          "debug_webhook_url": "https://example.com",
          "digit_termiantors": "string",
          "direction": [
            "string"
          ]
        },
        "post_prompt": {
          "confidence": 1,
          "frequency_penalty": 1,
          "presence_penalty": 1,
          "temperature": 1,
          "text": "string",
          "top_p": 1
        },
        "prompt": {
          "confidence": 1,
          "contexts": {
            "default": {
              "steps": [
                {}
              ]
            }
          },
          "frequency_penalty": 1,
          "presence_penalty": 1,
          "temperature": 1,
          "text": "string",
          "top_p": 1
        }
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_agent.agent_id` | string | Unique ID of an AI Agent. |
| `ai_agent.name` | string | Name of the AI Agent. |
| `ai_agent.params.acknowledge_interruptions` | boolean | Instructs the agent to acknowledge crosstalk and confirm user input when the user speaks over the agent. |
| `ai_agent.params.ai_name` | string | Sets the name the AI agent responds to for wake/activation purposes. When using `enable_pause`, `start_paused`, or `speak_when_spoken_to`, the user must say this name to get the agent's attention. |
| `ai_agent.params.ai_volume` | number | Adjust the volume of the AI. Allowed values from `-50` - `50`. |
| `ai_agent.params.app_name` | string | A custom identifier for the AI application instance. This name is included in webhook payloads. |
| `ai_agent.params.attention_timeout` | number | Amount of time, in ms, to wait before prompting the user to respond. Allowed values from `10,000` - `600,000`. Set to `0` to disable. |
| `ai_agent.params.attention_timeout_prompt` | string | A custom prompt that is fed into the AI when the attention_timeout is reached. |
| `ai_agent.params.background_file` | string | URL of audio file to play in the background while AI plays in foreground. |
| `ai_agent.params.background_file_loops` | number | Maximum number of times to loop playing the background file. `undefined` means loop indefinitely. |
| `ai_agent.params.background_file_volume` | number | Defines background_file volume within a range of `-50` to `50`. |
| `ai_agent.params.barge_match_string` | string | Takes a string, including a regular expression, defining barge behavior. For example, this param can direct the AI to stop when the word 'hippopotomus' is input. |
| `ai_agent.params.barge_min_words` | number | Defines the number of words that must be input before triggering barge behavior, in a range of `1-99`. |
| `ai_agent.params.conscience` | string | Sets the prompt which binds the agent to its purpose. |
| `ai_agent.params.conversation_id` | string | Used by `check_for_input` and `save_conversation` to identify an individual conversation. |
| `ai_agent.params.convo` | array<object> | Injects pre-existing conversation history into the AI session at startup. This allows you to seed the AI agent with context from a previous conversation or provide example interactions. |
| `ai_agent.params.debug` | boolean | Enables debug mode for the AI session. |
| `ai_agent.params.debug_webhook_level` | number | Enables debugging to the set URL. Allowed values from `0` - `1`. |
| `ai_agent.params.debug_webhook_url` | string | Each interaction between the AI and end user is posted in real time to the established URL. |
| `ai_agent.params.digit_termiantors` | string | DTMF digit, as a string, to signal the end of input (ex: '#') |
| `ai_agent.params.direction` | array<string> | Forces the direction of the call to the assistant. Valid values are `inbound` and `outbound`. |
| `ai_agent.post_prompt.confidence` | number | Threshold to fire a speech-detect event at the end of the utterance. Float value between 0.0 and 1.0. Decreasing this value will reduce the pause after the user speaks, but may introduce false positives. |
| `ai_agent.post_prompt.frequency_penalty` | number | Aversion to repeating lines. Float value between -2.0 and 2.0. Positive values decrease the model's likelihood to repeat the same line verbatim. |
| `ai_agent.post_prompt.presence_penalty` | number | Aversion to staying on topic. Float value between -2.0 and 2.0. Positive values increase the model's likelihood to talk about new topics. |
| `ai_agent.post_prompt.temperature` | number | Randomness setting. Float value between 0.0 and 1.5. Closer to 0 will make the output less random. |
| `ai_agent.post_prompt.text` | string | The instructions to send to the agent. |
| `ai_agent.post_prompt.top_p` | number | Randomness setting. Alternative to `temperature`. Float value between 0.0 and 1.0. Closer to 0 will make the output less random. |
| `ai_agent.prompt.confidence` | number | Threshold to fire a speech-detect event at the end of the utterance. Float value between 0.0 and 1.0. Decreasing this value will reduce the pause after the user speaks, but may introduce false positives. |
| `ai_agent.prompt.contexts.default.steps` | array<object> | An array of objects that define the steps in the context. These steps are used to define the flow of the conversation. |
| `ai_agent.prompt.frequency_penalty` | number | Aversion to repeating lines. Float value between -2.0 and 2.0. Positive values decrease the model's likelihood to repeat the same line verbatim. |
| `ai_agent.prompt.presence_penalty` | number | Aversion to staying on topic. Float value between -2.0 and 2.0. Positive values increase the model's likelihood to talk about new topics. |
| `ai_agent.prompt.temperature` | number | Randomness setting. Float value between 0.0 and 1.5. Closer to 0 will make the output less random. |
| `ai_agent.prompt.text` | string | The instructions to send to the agent. |
| `ai_agent.prompt.top_p` | number | Randomness setting. Alternative to `temperature`. Float value between 0.0 and 1.0. Closer to 0 will make the output less random. |
| `created_at` | date | Date and time when the resource was created. |
| `display_name` | string | Display name of the Resource |
| `id` | string | Unique ID of the Resource. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | The type of Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

