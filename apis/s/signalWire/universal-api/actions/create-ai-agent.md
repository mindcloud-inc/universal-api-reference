# SignalWire: Create AI Agent

Creates a new AI agent in SignalWire.

```
POST https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-ai-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-ai-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/create-ai-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | Unique ID of an AI Agent. |
| `name` | string | yes | Name of the AI Agent. |
| `prompt.text` | string | no | The instructions to send to the agent. |
| `prompt.temperature` | number | no | Randomness setting. Float value between 0.0 and 1.5. Closer to 0 will make the output less random. |
| `prompt.topP` | number | no | Randomness setting. Alternative to `temperature`. Float value between 0.0 and 1.0. Closer to 0 will make the output less random. |
| `prompt.confidence` | number | no | Threshold to fire a speech-detect event at the end of the utterance. Float value between 0.0 and 1.0. Decreasing this value will reduce the pause after the user speaks, but may introduce false positives. |
| `prompt.presencePenalty` | number | no | Aversion to staying on topic. Float value between -2.0 and 2.0. Positive values increase the model's likelihood to talk about new topics. |
| `prompt.frequencyPenalty` | number | no | Aversion to repeating lines. Float value between -2.0 and 2.0. Positive values decrease the model's likelihood to repeat the same line verbatim. |
| `prompt.contexts.default.steps[]` | array<object> | no | An array of objects that define the steps in the context. These steps are used to define the flow of the conversation. |
| `prompt.contexts.default.steps[]` | array<object> | no | An array of objects that define the steps in the context. These steps are used to define the flow of the conversation. |
| `postPrompt.text` | string | no | The instructions to send to the agent. |
| `postPrompt.temperature` | number | no | Randomness setting. Float value between 0.0 and 1.5. Closer to 0 will make the output less random. |
| `postPrompt.topP` | number | no | Randomness setting. Alternative to `temperature`. Float value between 0.0 and 1.0. Closer to 0 will make the output less random. |
| `postPrompt.confidence` | number | no | Threshold to fire a speech-detect event at the end of the utterance. Float value between 0.0 and 1.0. Decreasing this value will reduce the pause after the user speaks, but may introduce false positives. |
| `postPrompt.presencePenalty` | number | no | Aversion to staying on topic. Float value between -2.0 and 2.0. Positive values increase the model's likelihood to talk about new topics. |
| `postPrompt.frequencyPenalty` | number | no | Aversion to repeating lines. Float value between -2.0 and 2.0. Positive values decrease the model's likelihood to repeat the same line verbatim. |
| `params.acknowledgeInterruptions` | boolean | no | Instructs the agent to acknowledge crosstalk and confirm user input when the user speaks over the agent. |
| `params.aiName` | string | no | Sets the name the AI agent responds to for wake/activation purposes. When using `enable_pause`, `start_paused`, or `speak_when_spoken_to`, the user must say this name to get the agent's attention. |
| `params.aiVolume` | number | no | Adjust the volume of the AI. Allowed values from `-50` - `50`. |
| `params.appName` | string | no | A custom identifier for the AI application instance. This name is included in webhook payloads. |
| `params.attentionTimeout` | number | no | Amount of time, in ms, to wait before prompting the user to respond. Allowed values from `10,000` - `600,000`. Set to `0` to disable. |
| `params.attentionTimeoutPrompt` | string | no | A custom prompt that is fed into the AI when the attention_timeout is reached. |
| `params.backgroundFile` | string | no | URL of audio file to play in the background while AI plays in foreground. |
| `params.backgroundFileLoops` | number | no | Maximum number of times to loop playing the background file. `undefined` means loop indefinitely. |
| `params.backgroundFileVolume` | number | no | Defines background_file volume within a range of `-50` to `50`. |
| `params.bargeMatchString` | string | no | Takes a string, including a regular expression, defining barge behavior. For example, this param can direct the AI to stop when the word 'hippopotomus' is input. |
| `params.bargeMinWords` | number | no | Defines the number of words that must be input before triggering barge behavior, in a range of `1-99`. |
| `params.conscience` | string | no | Sets the prompt which binds the agent to its purpose. |
| `params.convo[]` | array<object> | no | Injects pre-existing conversation history into the AI session at startup. This allows you to seed the AI agent with context from a previous conversation or provide example interactions. |
| `params.convo[]` | array<object> | no | Injects pre-existing conversation history into the AI session at startup. This allows you to seed the AI agent with context from a previous conversation or provide example interactions. |
| `params.conversationId` | string | no | Used by `check_for_input` and `save_conversation` to identify an individual conversation. |
| `params.debugWebhookLevel` | number | no | Enables debugging to the set URL. Allowed values from `0` - `1`. |
| `params.debugWebhookUrl` | string | no | Each interaction between the AI and end user is posted in real time to the established URL. |
| `params.debug` | boolean | no | Enables debug mode for the AI session. |
| `params.direction[]` | array<string> | no | Forces the direction of the call to the assistant. Valid values are `inbound` and `outbound`. |
| `params.direction[]` | array<string> | no | Forces the direction of the call to the assistant. Valid values are `inbound` and `outbound`. |
| `params.digitTermiantors` | string | no | DTMF digit, as a string, to signal the end of input (ex: '#') |
| `params.digitTimeout` | number | no | Time, in ms, at the end of digit input to detect end of input. Allowed values from `250` - `10,000`. |
| `params.endOfSpeechTimeout` | number | no | Amount of silence, in ms, at the end of an utterance to detect end of speech. Allowed values from `250` - `10,000`. |
| `params.enableInnerDialog` | boolean | no | Enables the inner dialog feature for background conversation analysis. |
| `params.enablePause` | boolean | no | Enables the pause/resume functionality for the AI agent. |
| `params.enableTurnDetection` | boolean | no | Enables intelligent turn detection that monitors partial speech transcripts. |
| `params.elevenLabsStability` | number | no | The stability slider determines how stable the voice is and the randomness between each generation. Lowering this slider introduces a broader emotional range for the voice. |
| `params.elevenLabsSimilarity` | number | no | The similarity slider dictates how closely the AI should adhere to the original voice when attempting to replicate it. The higher the similarity, the closer the AI will sound to the original voice. |
| `params.energyLevel` | number | no | Amount of energy necessary for bot to hear you (in dB). Allowed values from `0.0` - `100.0`. |
| `params.holdMusic` | string | no | A URL for the hold music to play, accepting WAV, mp3, and FreeSWITCH tone_stream. |
| `params.holdOnProcess` | boolean | no | Enables hold music during SWAIG processing. |
| `params.inactivityTimeout` | number | no | Amount of time, in ms, to wait before exiting the app due to inactivity. Allowed values from `10,000` - `3,600,000`. |
| `params.innerDialogModel` | string | no | Specifies the AI model to use for the inner dialog feature. |
| `params.innerDialogPrompt` | string | no | The system prompt that guides the inner dialog AI's behavior. |
| `params.innerDialogSynced` | boolean | no | When enabled, synchronizes the inner dialog with the main conversation flow. |
| `params.inputPollFreq` | string | no | Check for input function with check_for_input. Example use case: Feeding an inbound SMS to AI on a voice call, eg., for collecting an email address or other complex information. |
| `params.interruptOnNoise` | boolean | no | When enabled, barges agent upon any sound interruption longer than 1 second. |
| `params.interruptPrompt` | string | no | Provide a prompt for the agent to handle crosstalk. |
| `params.languagesEnabled` | boolean | no | Allows multilingualism when `true`. |
| `params.localTz` | string | no | The local timezone setting for the AI. Value should use `IANA TZ ID` |
| `params.maxResponseTokens` | number | no | Sets the maximum number of tokens the AI model can generate in a single response. |
| `params.outboundAttentionTimeout` | number | no | Sets a time duration for the outbound call recipient to respond to the AI agent before timeout, in a range from `10000` to `600000`. |
| `params.persistGlobalData` | boolean | no | When enabled, global_data persists across multiple AI agent invocations within the same call. |
| `params.pomFormat` | string | no | Specifies the output format for structured prompts. Valid values are `markdown` or `xml`. |
| `params.saveConversation` | boolean | no | Send a summary of the conversation after the call ends. This requires a `post_url` to be set in the ai parameters and the `conversation_id` defined below. This eliminates the need for a `post_prompt` in the ai parameters. |
| `params.speakWhenSpokenTo` | boolean | no | When enabled, the AI agent remains silent until directly addressed by name. |
| `params.startPaused` | boolean | no | When enabled, the AI agent starts in a paused state. |
| `params.swaigAllowSettings` | boolean | no | Allows tweaking any of the indicated settings, such as `barge_match_string`, using the returned SWML from the SWAIG function. |
| `params.swaigAllowSwml` | boolean | no | Allows your SWAIG to return SWML to be executed. |
| `params.swaigPostConversation` | boolean | no | Post entire conversation to any SWAIG call. |
| `params.swaigPostSwmlVars` | boolean | no | Controls whether SWML variables are included in SWAIG function webhook payloads. |
| `params.transferSummary` | boolean | no | Pass a summary of a conversation from one AI agent to another. For example, transfer a call summary between support agents in two departments. |
| `params.turnDetectionTimeout` | number | no | Time in milliseconds to wait after detecting a potential end-of-turn before finalizing speech recognition. |
| `params.vadConfig` | string | no | Configures Silero Voice Activity Detection (VAD) settings. Format: `threshold` or `threshold:frame_ms`. The threshold (0-100) sets sensitivity for detecting voice activity. The optional frame_ms (16-40) sets frame duration in milliseconds. |
| `params.verboseLogs` | boolean | no | Enable verbose logging. |
| `params.waitForUser` | boolean | no | When false, AI agent will initialize dialogue after call is setup. When true, agent will wait for the user to speak first. |
| `params.wakePrefix` | string | no | Specifies an additional prefix that must be spoken along with the agent's name to wake the agent. |
| `pronounce[]` | array<object> | no | An array of JSON objects to clarify the AI's pronunciation of words or expressions. |
| `hints[]` | array<string> | no | An array of hints (as strings) to provide context to the dialogue. |
| `languages[]` | array<object> | no | An array of JSON objects defining supported languages in the conversation. |
| `swaig.defaults.webHookUrl` | string | no | Default URL to send status callbacks and reports to. Authentication can also be set in the url in the format of `username:password@url.` |
| `swaig.nativeFunctions[]` | array<string> | no | Prebuilt functions the AI agent is able to call from this list of available native functions |
| `swaig.includes[]` | array<object> | no | An array of objects to include remote function signatures. The object fields are url to specify where the remote functions are defined and functions which is an array of the function names as strings. |
| `swaig.functions[]` | array<object> | no | An array of JSON objects to define functions that can be executed during the interaction with the AI. Default is not set. The fields of this object are the six following. |

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
| `display_name` | string | Display name of the AIAgent Fabric Resource |
| `id` | string | Unique ID of the AIAgent. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `POST /fabric/resources/ai_agents` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ai-agent.md) for the provider-specific parameters and requirements.

