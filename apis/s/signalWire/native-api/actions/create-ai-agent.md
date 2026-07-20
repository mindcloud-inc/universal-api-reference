# Create AI Agent with SignalWire

Creates a new AI agent in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/ai_agents`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create AI Agent](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/create-ai-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | yes | Unique ID of an AI Agent. |
| `name` | body | `string` | yes | Name of the AI Agent. |
| `prompt.text` | body | `string` | no | The instructions to send to the agent. |
| `prompt.temperature` | body | `number` | no | Randomness setting. Float value between 0.0 and 1.5. Closer to 0 will make the output less random. |
| `prompt.top_p` | body | `number` | no | Randomness setting. Alternative to `temperature`. Float value between 0.0 and 1.0. Closer to 0 will make the output less random. |
| `prompt.confidence` | body | `number` | no | Threshold to fire a speech-detect event at the end of the utterance. Float value between 0.0 and 1.0. Decreasing this value will reduce the pause after the user speaks, but may introduce false positives. |
| `prompt.presence_penalty` | body | `number` | no | Aversion to staying on topic. Float value between -2.0 and 2.0. Positive values increase the model's likelihood to talk about new topics. |
| `prompt.frequency_penalty` | body | `number` | no | Aversion to repeating lines. Float value between -2.0 and 2.0. Positive values decrease the model's likelihood to repeat the same line verbatim. |
| `prompt.contexts.default.steps[]` | body | `array<object>` | no | An array of objects that define the steps in the context. These steps are used to define the flow of the conversation. |
| `prompt.contexts.default.steps[]` | body | `array<object>` | no | An array of objects that define the steps in the context. These steps are used to define the flow of the conversation. |
| `post_prompt.text` | body | `string` | no | The instructions to send to the agent. |
| `post_prompt.temperature` | body | `number` | no | Randomness setting. Float value between 0.0 and 1.5. Closer to 0 will make the output less random. |
| `post_prompt.top_p` | body | `number` | no | Randomness setting. Alternative to `temperature`. Float value between 0.0 and 1.0. Closer to 0 will make the output less random. |
| `post_prompt.confidence` | body | `number` | no | Threshold to fire a speech-detect event at the end of the utterance. Float value between 0.0 and 1.0. Decreasing this value will reduce the pause after the user speaks, but may introduce false positives. |
| `post_prompt.presence_penalty` | body | `number` | no | Aversion to staying on topic. Float value between -2.0 and 2.0. Positive values increase the model's likelihood to talk about new topics. |
| `post_prompt.frequency_penalty` | body | `number` | no | Aversion to repeating lines. Float value between -2.0 and 2.0. Positive values decrease the model's likelihood to repeat the same line verbatim. |
| `params.acknowledge_interruptions` | body | `boolean` | no | Instructs the agent to acknowledge crosstalk and confirm user input when the user speaks over the agent. |
| `params.ai_name` | body | `string` | no | Sets the name the AI agent responds to for wake/activation purposes. When using `enable_pause`, `start_paused`, or `speak_when_spoken_to`, the user must say this name to get the agent's attention. |
| `params.ai_volume` | body | `number` | no | Adjust the volume of the AI. Allowed values from `-50` - `50`. |
| `params.app_name` | body | `string` | no | A custom identifier for the AI application instance. This name is included in webhook payloads. |
| `params.attention_timeout` | body | `number` | no | Amount of time, in ms, to wait before prompting the user to respond. Allowed values from `10,000` - `600,000`. Set to `0` to disable. |
| `params.attention_timeout_prompt` | body | `string` | no | A custom prompt that is fed into the AI when the attention_timeout is reached. |
| `params.background_file` | body | `string` | no | URL of audio file to play in the background while AI plays in foreground. |
| `params.background_file_loops` | body | `number` | no | Maximum number of times to loop playing the background file. `undefined` means loop indefinitely. |
| `params.background_file_volume` | body | `number` | no | Defines background_file volume within a range of `-50` to `50`. |
| `params.barge_match_string` | body | `string` | no | Takes a string, including a regular expression, defining barge behavior. For example, this param can direct the AI to stop when the word 'hippopotomus' is input. |
| `params.barge_min_words` | body | `number` | no | Defines the number of words that must be input before triggering barge behavior, in a range of `1-99`. |
| `params.conscience` | body | `string` | no | Sets the prompt which binds the agent to its purpose. |
| `params.convo[]` | body | `array<object>` | no | Injects pre-existing conversation history into the AI session at startup. This allows you to seed the AI agent with context from a previous conversation or provide example interactions. |
| `params.convo[]` | body | `array<object>` | no | Injects pre-existing conversation history into the AI session at startup. This allows you to seed the AI agent with context from a previous conversation or provide example interactions. |
| `params.conversation_id` | body | `string` | no | Used by `check_for_input` and `save_conversation` to identify an individual conversation. |
| `params.debug_webhook_level` | body | `number` | no | Enables debugging to the set URL. Allowed values from `0` - `1`. |
| `params.debug_webhook_url` | body | `string` | no | Each interaction between the AI and end user is posted in real time to the established URL. |
| `params.debug` | body | `boolean` | no | Enables debug mode for the AI session. |
| `params.direction[]` | body | `array<string>` | no | Forces the direction of the call to the assistant. Valid values are `inbound` and `outbound`. |
| `params.direction[]` | body | `array<string>` | no | Forces the direction of the call to the assistant. Valid values are `inbound` and `outbound`. |
| `params.digit_termiantors` | body | `string` | no | DTMF digit, as a string, to signal the end of input (ex: '#') |
| `params.digit_timeout` | body | `number` | no | Time, in ms, at the end of digit input to detect end of input. Allowed values from `250` - `10,000`. |
| `params.end_of_speech_timeout` | body | `number` | no | Amount of silence, in ms, at the end of an utterance to detect end of speech. Allowed values from `250` - `10,000`. |
| `params.enable_inner_dialog` | body | `boolean` | no | Enables the inner dialog feature for background conversation analysis. |
| `params.enable_pause` | body | `boolean` | no | Enables the pause/resume functionality for the AI agent. |
| `params.enable_turn_detection` | body | `boolean` | no | Enables intelligent turn detection that monitors partial speech transcripts. |
| `params.eleven_labs_stability` | body | `number` | no | The stability slider determines how stable the voice is and the randomness between each generation. Lowering this slider introduces a broader emotional range for the voice. |
| `params.eleven_labs_similarity` | body | `number` | no | The similarity slider dictates how closely the AI should adhere to the original voice when attempting to replicate it. The higher the similarity, the closer the AI will sound to the original voice. |
| `params.energy_level` | body | `number` | no | Amount of energy necessary for bot to hear you (in dB). Allowed values from `0.0` - `100.0`. |
| `params.hold_music` | body | `string` | no | A URL for the hold music to play, accepting WAV, mp3, and FreeSWITCH tone_stream. |
| `params.hold_on_process` | body | `boolean` | no | Enables hold music during SWAIG processing. |
| `params.inactivity_timeout` | body | `number` | no | Amount of time, in ms, to wait before exiting the app due to inactivity. Allowed values from `10,000` - `3,600,000`. |
| `params.inner_dialog_model` | body | `string` | no | Specifies the AI model to use for the inner dialog feature. |
| `params.inner_dialog_prompt` | body | `string` | no | The system prompt that guides the inner dialog AI's behavior. |
| `params.inner_dialog_synced` | body | `boolean` | no | When enabled, synchronizes the inner dialog with the main conversation flow. |
| `params.input_poll_freq` | body | `string` | no | Check for input function with check_for_input. Example use case: Feeding an inbound SMS to AI on a voice call, eg., for collecting an email address or other complex information. |
| `params.interrupt_on_noise` | body | `boolean` | no | When enabled, barges agent upon any sound interruption longer than 1 second. |
| `params.interrupt_prompt` | body | `string` | no | Provide a prompt for the agent to handle crosstalk. |
| `params.languages_enabled` | body | `boolean` | no | Allows multilingualism when `true`. |
| `params.local_tz` | body | `string` | no | The local timezone setting for the AI. Value should use `IANA TZ ID` |
| `params.max_response_tokens` | body | `number` | no | Sets the maximum number of tokens the AI model can generate in a single response. |
| `params.outbound_attention_timeout` | body | `number` | no | Sets a time duration for the outbound call recipient to respond to the AI agent before timeout, in a range from `10000` to `600000`. |
| `params.persist_global_data` | body | `boolean` | no | When enabled, global_data persists across multiple AI agent invocations within the same call. |
| `params.pom_format` | body | `string` | no | Specifies the output format for structured prompts. Valid values are `markdown` or `xml`. |
| `params.save_conversation` | body | `boolean` | no | Send a summary of the conversation after the call ends. This requires a `post_url` to be set in the ai parameters and the `conversation_id` defined below. This eliminates the need for a `post_prompt` in the ai parameters. |
| `params.speak_when_spoken_to` | body | `boolean` | no | When enabled, the AI agent remains silent until directly addressed by name. |
| `params.start_paused` | body | `boolean` | no | When enabled, the AI agent starts in a paused state. |
| `params.swaig_allow_settings` | body | `boolean` | no | Allows tweaking any of the indicated settings, such as `barge_match_string`, using the returned SWML from the SWAIG function. |
| `params.swaig_allow_swml` | body | `boolean` | no | Allows your SWAIG to return SWML to be executed. |
| `params.swaig_post_conversation` | body | `boolean` | no | Post entire conversation to any SWAIG call. |
| `params.swaig_post_swml_vars` | body | `boolean` | no | Controls whether SWML variables are included in SWAIG function webhook payloads. |
| `params.transfer_summary` | body | `boolean` | no | Pass a summary of a conversation from one AI agent to another. For example, transfer a call summary between support agents in two departments. |
| `params.turn_detection_timeout` | body | `number` | no | Time in milliseconds to wait after detecting a potential end-of-turn before finalizing speech recognition. |
| `params.vad_config` | body | `string` | no | Configures Silero Voice Activity Detection (VAD) settings. Format: `threshold` or `threshold:frame_ms`. The threshold (0-100) sets sensitivity for detecting voice activity. The optional frame_ms (16-40) sets frame duration in milliseconds. |
| `params.verbose_logs` | body | `boolean` | no | Enable verbose logging. |
| `params.wait_for_user` | body | `boolean` | no | When false, AI agent will initialize dialogue after call is setup. When true, agent will wait for the user to speak first. |
| `params.wake_prefix` | body | `string` | no | Specifies an additional prefix that must be spoken along with the agent's name to wake the agent. |
| `pronounce[]` | body | `array<object>` | no | An array of JSON objects to clarify the AI's pronunciation of words or expressions. |
| `hints[]` | body | `array<string>` | no | An array of hints (as strings) to provide context to the dialogue. |
| `languages[]` | body | `array<object>` | no | An array of JSON objects defining supported languages in the conversation. |
| `SWAIG.defaults.web_hook_url` | body | `string` | no | Default URL to send status callbacks and reports to. Authentication can also be set in the url in the format of `username:password@url.` |
| `SWAIG.native_functions[]` | body | `array<string>` | no | Prebuilt functions the AI agent is able to call from this list of available native functions |
| `SWAIG.includes[]` | body | `array<object>` | no | An array of objects to include remote function signatures. The object fields are url to specify where the remote functions are defined and functions which is an array of the function names as strings. |
| `SWAIG.functions[]` | body | `array<object>` | no | An array of JSON objects to define functions that can be executed during the interaction with the AI. Default is not set. The fields of this object are the six following. |
