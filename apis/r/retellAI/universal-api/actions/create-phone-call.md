# Retell AI: Create Phone Call

Creates a phone call in Retell AI.

```
POST https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-phone-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-phone-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentOverride.agent.piiConfig.categories[]": [
    "string"
  ],
  "fromNumber": "string",
  "toNumber": "string",
  "agentOverride.agent.responseEngine.type": "string",
  "agentOverride.agent.responseEngine.llmId": "string",
  "agentOverride.agent.pronunciationDictionary[].word": "string",
  "agentOverride.agent.pronunciationDictionary[].alphabet": "string",
  "agentOverride.agent.pronunciationDictionary[].phoneme": "string",
  "agentOverride.agent.voicemailOption.action": {},
  "agentOverride.agent.voicemailOption.action.type": "ava@example.com",
  "agentOverride.agent.voicemailOption.action.text": "ava@example.com",
  "agentOverride.agent.ivrOption.action": {},
  "agentOverride.agent.ivrOption.action.type": "string",
  "agentOverride.agent.postCallAnalysisData[].type": "string",
  "agentOverride.agent.postCallAnalysisData[].name": "Ava Chen",
  "agentOverride.agent.postCallAnalysisData[].description": "string",
  "agentOverride.agent.customSttConfig.provider": "string",
  "agentOverride.agent.customSttConfig.endpointingMs": 1,
  "agentOverride.agent.piiConfig.mode": "string",
  "agentOverride.conversationFlow.modelChoice.type": "string",
  "agentOverride.conversationFlow.modelChoice.model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/create-phone-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentOverride.agent.piiConfig.categories[]": ["string"],
    "fromNumber": "string",
    "toNumber": "string",
    "agentOverride.agent.responseEngine.type": "string",
    "agentOverride.agent.responseEngine.llmId": "string",
    "agentOverride.agent.pronunciationDictionary[].word": "string",
    "agentOverride.agent.pronunciationDictionary[].alphabet": "string",
    "agentOverride.agent.pronunciationDictionary[].phoneme": "string",
    "agentOverride.agent.voicemailOption.action": {},
    "agentOverride.agent.voicemailOption.action.type": "ava@example.com",
    "agentOverride.agent.voicemailOption.action.text": "ava@example.com",
    "agentOverride.agent.ivrOption.action": {},
    "agentOverride.agent.ivrOption.action.type": "string",
    "agentOverride.agent.postCallAnalysisData[].type": "string",
    "agentOverride.agent.postCallAnalysisData[].name": "Ava Chen",
    "agentOverride.agent.postCallAnalysisData[].description": "string",
    "agentOverride.agent.customSttConfig.provider": "string",
    "agentOverride.agent.customSttConfig.endpointingMs": 1,
    "agentOverride.agent.piiConfig.mode": "string",
    "agentOverride.agent.piiConfig.categories[]": ["string"],
    "agentOverride.agent.piiConfig.categories[]": ["string"],
    "agentOverride.conversationFlow.modelChoice.type": "string",
    "agentOverride.conversationFlow.modelChoice.model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentOverride.agent.backchannelWords[]` | array<string> | no | Only applicable when enable_backchannel is true. A list of words that the agent would use as backchannel. If not set, default backchannel words will apply. Check out [backchannel default words](/agent/interaction-configuration#backchannel) for more details. Note that certain voices do not work too well with certain words, so it's recommended to experiment before adding any words. |
| `agentOverride.agent.boostedKeywords[]` | array<string> | no | Provide a customized list of keywords to bias the transcriber model, so that these words are more likely to get transcribed. Commonly used for names, brands, street, etc. |
| `agentOverride.agent.fallbackVoiceIds[]` | array<string> | no | When TTS provider for the selected voice is experiencing outages, we would use fallback voices listed here for the agent. Voice id and the fallback voice ids must be from different TTS providers. The system would go through the list in order, if the first one in the list is also having outage, it would use the next one. Set to null to remove voice fallback for the agent. |
| `agentOverride.agent.guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `agentOverride.agent.guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `agentOverride.agent.piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `agentOverride.agent.postCallAnalysisData[]` | array<object> | no | Post call analysis data to extract from the call. This data will augment the pre-defined variables extracted in the call analysis. This will be available after the call ends. |
| `agentOverride.agent.postCallAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `agentOverride.agent.pronunciationDictionary[]` | array<object> | no | A list of words / phrases and their pronunciation to be used to guide the audio synthesize for consistent pronunciation. Check the dashboard to see what provider supports this feature. Set to null to remove pronunciation dictionary from this agent. |
| `agentOverride.agent.webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to call_started, call_ended, call_analyzed. |
| `agentOverride.conversationFlow.knowledgeBaseIds[]` | array<string> | no | Knowledge base IDs for RAG (Retrieval-Augmented Generation). |
| `agentOverride.retellLlm.knowledgeBaseIds[]` | array<string> | no | A list of knowledge base ids to use for this resource. |
| `fromNumber` | string | yes | The number you own in E.164 format. Must be a number purchased from Retell or imported to Retell. |
| `toNumber` | string | yes | The number you want to call, in E.164 format. If using a number purchased from Retell, only US numbers are supported as destination. |
| `overrideAgentId` | string | no | For this particular call, override the agent used with this agent id. This does not bind the agent to this number, this is for one time override. |
| `overrideAgentVersion` | number | no | For this particular call, override the agent version used with this version. This does not bind the agent version to this number, this is for one time override. |
| `agentOverride` | object | no | Override configuration for agent, retell LLM, or conversation flow settings for a specific call. |
| `agentOverride.agent` | object | no |  |
| `agentOverride.agent.responseEngine` | object | no |  |
| `agentOverride.agent.responseEngine.type` | string | yes | type of the Response Engine. Allowed values: retell-llm. |
| `agentOverride.agent.responseEngine.llmId` | string | yes | id of the Retell LLM Response Engine. |
| `agentOverride.agent.responseEngine.version` | number | no | Version of the Retell LLM Response Engine. |
| `agentOverride.agent.agentName` | string | no | The name of the agent. Only used for your own reference. |
| `agentOverride.agent.versionDescription` | string | no | Optional description of the agent version. Used for your own reference and documentation. |
| `agentOverride.agent.voiceId` | string | no | Unique voice id used for the agent. Find list of available voices and their preview in Dashboard. |
| `agentOverride.agent.voiceModel` | string | no | Select the voice model used for the selected voice. Each provider has a set of available voice models. Set to null to remove voice model selection, and default ones will apply. Check out dashboard for more details of each voice model. |
| `agentOverride.agent.fallbackVoiceIds[]` | array<string> | no | When TTS provider for the selected voice is experiencing outages, we would use fallback voices listed here for the agent. Voice id and the fallback voice ids must be from different TTS providers. The system would go through the list in order, if the first one in the list is also having outage, it would use the next one. Set to null to remove voice fallback for the agent. |
| `agentOverride.agent.fallbackVoiceIds[]` | array<string> | no | When TTS provider for the selected voice is experiencing outages, we would use fallback voices listed here for the agent. Voice id and the fallback voice ids must be from different TTS providers. The system would go through the list in order, if the first one in the list is also having outage, it would use the next one. Set to null to remove voice fallback for the agent. |
| `agentOverride.agent.voiceTemperature` | number | no | Controls how stable the voice is. Value ranging from [0,2]. Lower value means more stable, and higher value means more variant speech generation. Check the dashboard to see what provider supports this feature. If unset, default value 1 will apply. |
| `agentOverride.agent.voiceSpeed` | number | no | Controls speed of voice. Value ranging from [0.5,2]. Lower value means slower speech, while higher value means faster speech rate. If unset, default value 1 will apply. |
| `agentOverride.agent.enableDynamicVoiceSpeed` | boolean | no | If set to true, will enable dynamic voice speed adjustment based on the user's speech rate and conversation context. If unset, default value false will apply. |
| `agentOverride.agent.enableDynamicResponsiveness` | boolean | no | If set to true, the agent will dynamically adjust how quickly it responds based on the user's speech rate and past turn-taking behavior in the call. If unset, default value false will apply. |
| `agentOverride.agent.volume` | number | no | If set, will control the volume of the agent. Value ranging from [0,2]. Lower value means quieter agent speech, while higher value means louder agent speech. If unset, default value 1 will apply. |
| `agentOverride.agent.voiceEmotion` | string | no | Controls the emotional tone of the agent's voice. Currently supported for Cartesia and Minimax TTS providers. If unset, no emotion will be used. Allowed values: calm, sympathetic, happy, sad, angry, fearful, surprised. |
| `agentOverride.agent.responsiveness` | number | no | Controls how responsive is the agent. Value ranging from [0,1]. Lower value means less responsive agent (wait more, respond slower), while higher value means faster exchanges (respond when it can). If unset, default value 1 will apply. |
| `agentOverride.agent.interruptionSensitivity` | number | no | Controls how sensitive the agent is to user interruptions. Value ranging from [0,1]. Lower value means it will take longer / more words for user to interrupt agent, while higher value means it's easier for user to interrupt agent. If unset, default value 1 will apply. When this is set to 0, agent would never be interrupted. |
| `agentOverride.agent.enableBackchannel` | boolean | no | Controls whether the agent would backchannel (agent interjects the speaker with phrases like "yeah", "uh-huh" to signify interest and engagement). Backchannel when enabled tends to show up more in longer user utterances. If not set, agent will not backchannel. |
| `agentOverride.agent.backchannelFrequency` | number | no | Only applicable when enable_backchannel is true. Controls how often the agent would backchannel when a backchannel is possible. Value ranging from [0,1]. Lower value means less frequent backchannel, while higher value means more frequent backchannel. If unset, default value 0.8 will apply. |
| `agentOverride.agent.backchannelWords[]` | array<string> | no | Only applicable when enable_backchannel is true. A list of words that the agent would use as backchannel. If not set, default backchannel words will apply. Check out [backchannel default words](/agent/interaction-configuration#backchannel) for more details. Note that certain voices do not work too well with certain words, so it's recommended to experiment before adding any words. |
| `agentOverride.agent.backchannelWords[]` | array<string> | no | Only applicable when enable_backchannel is true. A list of words that the agent would use as backchannel. If not set, default backchannel words will apply. Check out [backchannel default words](/agent/interaction-configuration#backchannel) for more details. Note that certain voices do not work too well with certain words, so it's recommended to experiment before adding any words. |
| `agentOverride.agent.reminderTriggerMs` | number | no | If set (in milliseconds), will trigger a reminder to the agent to speak if the user has been silent for the specified duration after some agent speech. Must be a positive number. If unset, default value of 10000 ms (10 s) will apply. |
| `agentOverride.agent.reminderMaxCount` | number | no | If set, controls how many times agent would remind user when user is unresponsive. Must be a non negative integer. If unset, default value of 1 will apply (remind once). Set to 0 to disable agent from reminding. |
| `agentOverride.agent.ambientSound` | string | no | If set, will add ambient environment sound to the call to make experience more realistic. Currently supports the following options: - `coffee-shop`: Coffee shop ambience with people chatting in background. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/coffee-shop.wav) - `convention-hall`: Convention hall ambience, with some echo and people chatting in background. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/convention-hall.wav) - `summer-outdoor`: Summer outdoor ambience with cicada chirping. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/summer-outdoor.wav) - `mountain-outdoor`: Mountain outdoor ambience with birds singing. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/mountain-outdoor.wav) - `static-noise`: Constant static noise. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/static-noise.wav) - `call-center`: Call center work noise. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/call-center.wav) Set to `null` to remove ambient sound from this agent. Allowed values: coffee-shop, convention-hall, summer-outdoor, mountain-outdoor, static-noise, call-center. |
| `agentOverride.agent.ambientSoundVolume` | number | no | If set, will control the volume of the ambient sound. Value ranging from [0,2]. Lower value means quieter ambient sound, while higher value means louder ambient sound. If unset, default value 1 will apply. |
| `agentOverride.agent.language` | string | no | Specifies what language (and dialect) the speech recognition will operate in. For instance, selecting `en-GB` optimizes speech recognition for British English. If unset, will use default value `en-US`. Select `multi` for multilingual support. |
| `agentOverride.agent.webhookUrl` | string | no | The webhook for agent to listen to call events. See what events it would get at [webhook doc](/features/webhook). If set, will binds webhook events for this agent to the specified url, and will ignore the account level webhook for this agent. Set to `null` to remove webhook url from this agent. |
| `agentOverride.agent.webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to call_started, call_ended, call_analyzed. |
| `agentOverride.agent.webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to call_started, call_ended, call_analyzed. |
| `agentOverride.agent.webhookTimeoutMs` | number | no | The timeout for the webhook in milliseconds. If not set, default value of 10000 will apply. |
| `agentOverride.agent.boostedKeywords[]` | array<string> | no | Provide a customized list of keywords to bias the transcriber model, so that these words are more likely to get transcribed. Commonly used for names, brands, street, etc. |
| `agentOverride.agent.boostedKeywords[]` | array<string> | no | Provide a customized list of keywords to bias the transcriber model, so that these words are more likely to get transcribed. Commonly used for names, brands, street, etc. |
| `agentOverride.agent.dataStorageSetting` | string | no | Granular setting to manage how Retell stores sensitive data (transcripts, recordings, logs, etc.). This replaces the deprecated `opt_out_sensitive_data_storage` field. - `everything`: Store all data including transcripts, recordings, and logs. - `everything_except_pii`: Store data without PII when PII is detected. - `basic_attributes_only`: Store only basic attributes; no transcripts/recordings/logs. If not set, default value of "everything" will apply. Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `agentOverride.agent.dataStorageRetentionDays` | number | no | Number of days to retain call/chat data before automatic deletion. Must be between 1 and 730 days. If not set, data is retained forever (no automatic deletion). |
| `agentOverride.agent.optInSignedUrl` | boolean | no | Whether this agent opts in for signed URLs for public logs and recordings. When enabled, the generated URLs will include security signatures that restrict access and automatically expire after 24 hours. |
| `agentOverride.agent.signedUrlExpirationMs` | number | no | The expiration time for the signed url in milliseconds. Only applicable when opt_in_signed_url is true. If not set, default value of 86400000 (24 hours) will apply. |
| `agentOverride.agent.pronunciationDictionary[]` | array<object> | no | A list of words / phrases and their pronunciation to be used to guide the audio synthesize for consistent pronunciation. Check the dashboard to see what provider supports this feature. Set to null to remove pronunciation dictionary from this agent. |
| `agentOverride.agent.pronunciationDictionary[]` | array<object> | no | A list of words / phrases and their pronunciation to be used to guide the audio synthesize for consistent pronunciation. Check the dashboard to see what provider supports this feature. Set to null to remove pronunciation dictionary from this agent. |
| `agentOverride.agent.pronunciationDictionary[].word` | string | yes | The string of word / phrase to be annotated with pronunciation. |
| `agentOverride.agent.pronunciationDictionary[].alphabet` | string | yes | The phonetic alphabet to be used for pronunciation. Allowed values: ipa, cmu. |
| `agentOverride.agent.pronunciationDictionary[].phoneme` | string | yes | Pronunciation of the word in the format of a IPA / CMU pronunciation. |
| `agentOverride.agent.normalizeForSpeech` | boolean | no | If set to true, will normalize the some part of text (number, currency, date, etc) to spoken to its spoken form for more consistent speech synthesis (sometimes the voice synthesize system itself might read these wrong with the raw text). For example, it will convert "Call my number 2137112342 on Jul 5th, 2024 for the $24.12 payment" to "Call my number two one three seven one one two three four two on july fifth, twenty twenty four for the twenty four dollars twelve cents payment" before starting audio generation. |
| `agentOverride.agent.endCallAfterSilenceMs` | number | no | If users stay silent for a period after agent speech, end the call. The minimum value allowed is 10,000 ms (10 s). By default, this is set to 600000 (10 min). |
| `agentOverride.agent.maxCallDurationMs` | number | no | Maximum allowed length for the call, will force end the call if reached. The minimum value allowed is 60,000 ms (1 min), and maximum value allowed is 7,200,000 (2 hours). By default, this is set to 3,600,000 (1 hour). |
| `agentOverride.agent.enableVoicemailDetection` | boolean | no | If set to true, will detect whether the call enters a voicemail. Note that this feature is only available for phone calls. |
| `agentOverride.agent.voicemailMessage` | string | no | The message to be played when the call enters a voicemail. Note that this feature is only available for phone calls. If you want to hangup after hitting voicemail, set this to empty string. |
| `agentOverride.agent.voicemailDetectionTimeoutMs` | number | no | Configures when to stop running voicemail detection, as it becomes unlikely to hit voicemail after a couple minutes, and keep running it will only have negative impact. The minimum value allowed is 5,000 ms (5 s), and maximum value allowed is 180,000 (3 minutes). By default, this is set to 30,000 (30 s). |
| `agentOverride.agent.voicemailOption` | object | no | If this option is set, the call will try to detect voicemail in the first 3 minutes of the call. Actions defined (hangup, or leave a message) will be applied when the voicemail is detected. Set this to null to disable voicemail detection. |
| `agentOverride.agent.voicemailOption.action` | object | yes |  |
| `agentOverride.agent.voicemailOption.action.type` | string | yes | Allowed values: prompt. |
| `agentOverride.agent.voicemailOption.action.text` | string | yes | The prompt used to generate the text to be spoken when the call is detected to be in voicemail. |
| `agentOverride.agent.ivrOption` | object | no | If this option is set, the call will try to detect IVR in the first 3 minutes of the call. Actions defined will be applied when the IVR is detected. Set this to null to disable IVR detection. |
| `agentOverride.agent.ivrOption.action` | object | yes |  |
| `agentOverride.agent.ivrOption.action.type` | string | yes | Allowed values: hangup. |
| `agentOverride.agent.postCallAnalysisData[]` | array<object> | no | Post call analysis data to extract from the call. This data will augment the pre-defined variables extracted in the call analysis. This will be available after the call ends. |
| `agentOverride.agent.postCallAnalysisData[]` | array<object> | no | Post call analysis data to extract from the call. This data will augment the pre-defined variables extracted in the call analysis. This will be available after the call ends. |
| `agentOverride.agent.postCallAnalysisData[].type` | string | yes | Type of the variable to extract. Allowed values: string. |
| `agentOverride.agent.postCallAnalysisData[].name` | string | yes | Name of the variable. |
| `agentOverride.agent.postCallAnalysisData[].description` | string | yes | Description of the variable. |
| `agentOverride.agent.postCallAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `agentOverride.agent.postCallAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `agentOverride.agent.postCallAnalysisData[].required` | boolean | no | Whether this data is required. If true and the data is not extracted, the call will be marked as unsuccessful. |
| `agentOverride.agent.postCallAnalysisModel` | string | no | Available LLM models for agents. |
| `agentOverride.agent.analysisSuccessfulPrompt` | string | no | Prompt to determine whether the post call or chat analysis should mark the interaction as successful. Set to null to use the default prompt. |
| `agentOverride.agent.analysisSummaryPrompt` | string | no | Prompt to guide how the post call or chat analysis summary should be generated. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `agentOverride.agent.analysisUserSentimentPrompt` | string | no | Prompt to guide how the post call or chat analysis should evaluate user sentiment. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `agentOverride.agent.beginMessageDelayMs` | number | no | If set, will delay the first message by the specified amount of milliseconds, so that it gives user more time to prepare to take the call. Valid range is [0, 5000]. If not set or set to 0, agent will speak immediately. Only applicable when agent speaks first. |
| `agentOverride.agent.ringDurationMs` | number | no | If set, the phone ringing will last for the specified amount of milliseconds. This applies for both outbound call ringtime, and call transfer ringtime. Default to 30000 (30 s). Valid range is [5000, 300000]. |
| `agentOverride.agent.sttMode` | string | no | If set, determines whether speech to text should focus on latency or accuracy. Default to fast mode. When set to custom, custom_stt_config must be provided. Allowed values: fast, accurate, custom. |
| `agentOverride.agent.customSttConfig` | object | no | Custom STT configuration. Only used when stt_mode is set to custom. |
| `agentOverride.agent.customSttConfig.provider` | string | yes | The STT provider to use. Allowed values: azure, deepgram. |
| `agentOverride.agent.customSttConfig.endpointingMs` | number | yes | Endpointing timeout in milliseconds. Minimum is 100 for azure, 10 for deepgram. |
| `agentOverride.agent.vocabSpecialization` | string | no | If set, determines the vocabulary set to use for transcription. This setting only applies for English agents, for non English agent, this setting is a no-op. Default to general. Allowed values: general, medical. |
| `agentOverride.agent.allowUserDtmf` | boolean | no | If set to true, DTMF input will be accepted and processed. If false, any DTMF input will be ignored. Default to true. |
| `agentOverride.agent.userDtmfOptions` | object | no |  |
| `agentOverride.agent.userDtmfOptions.digitLimit` | number | no | The maximum number of digits allowed in the user's DTMF (Dual-Tone Multi-Frequency) input per turn. Once this limit is reached, the input is considered complete and a response will be generated immediately. |
| `agentOverride.agent.userDtmfOptions.terminationKey` | string | no | A single key that signals the end of DTMF input. Acceptable values include any digit (0-9), the pound/hash symbol (#), or the asterisk (*). |
| `agentOverride.agent.userDtmfOptions.timeoutMs` | number | no | The time (in milliseconds) to wait for user DTMF input before timing out. The timer resets with each digit received. |
| `agentOverride.agent.denoisingMode` | string | no | If set, determines what denoising mode to use. Use "no-denoise" to bypass all audio denoising. Default to noise-cancellation. Allowed values: no-denoise, noise-cancellation, noise-and-background-speech-cancellation. |
| `agentOverride.agent.piiConfig` | object | no |  |
| `agentOverride.agent.piiConfig.mode` | string | yes | The processing mode for PII scrubbing. Currently only post-call is supported. Allowed values: post_call. |
| `agentOverride.agent.piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `agentOverride.agent.piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `agentOverride.agent.guardrailConfig` | object | no |  |
| `agentOverride.agent.guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `agentOverride.agent.guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `agentOverride.agent.guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `agentOverride.agent.isPublic` | boolean | no | Whether the agent is public. When set to true, the agent is available for public agent preview link. |
| `agentOverride.retellLlm` | object | no | Override properties for Retell LLM configuration in agent override requests. |
| `agentOverride.retellLlm.model` | string | no | Available LLM models for agents. |
| `agentOverride.retellLlm.s2sModel` | string | no | Select the underlying speech to speech model. Can only set this or model, not both. Allowed values: gpt-4o-realtime, gpt-4o-mini-realtime, gpt-realtime, gpt-realtime-mini. |
| `agentOverride.retellLlm.modelTemperature` | number | no | If set, will control the randomness of the response. Value ranging from [0,1]. Lower value means more deterministic, while higher value means more random. If unset, default value 0 will apply. Note that for tool calling, a lower value is recommended. |
| `agentOverride.retellLlm.modelHighPriority` | boolean | no | If set to true, will use high priority pool with more dedicated resource to ensure lower and more consistent latency, default to false. This feature usually comes with a higher cost. |
| `agentOverride.retellLlm.toolCallStrictMode` | boolean | no | Whether to use strict mode for tool calls. Only applicable when using certain supported models. |
| `agentOverride.retellLlm.knowledgeBaseIds[]` | array<string> | no | A list of knowledge base ids to use for this resource. |
| `agentOverride.retellLlm.knowledgeBaseIds[]` | array<string> | no | A list of knowledge base ids to use for this resource. |
| `agentOverride.retellLlm.kbConfig` | object | no |  |
| `agentOverride.retellLlm.kbConfig.topK` | number | no | Max number of knowledge base chunks to retrieve |
| `agentOverride.retellLlm.kbConfig.filterScore` | number | no | Similarity threshold for filtering search results |
| `agentOverride.retellLlm.startSpeaker` | string | no | The speaker who starts the conversation. Required. Must be either 'user' or 'agent'. Allowed values: user, agent. |
| `agentOverride.retellLlm.beginAfterUserSilenceMs` | number | no | If set, the AI will begin the conversation after waiting for the user for the duration (in milliseconds) specified by this attribute. This only applies if the agent is configured to wait for the user to speak first. If not set, the agent will wait indefinitely for the user to speak. |
| `agentOverride.retellLlm.beginMessage` | string | no | First utterance said by the agent in the call. If not set, LLM will dynamically generate a message. If set to "", agent will wait for user to speak first. |
| `agentOverride.conversationFlow` | object | no | Override properties for conversation flow configuration in agent override requests. |
| `agentOverride.conversationFlow.modelChoice` | object | no |  |
| `agentOverride.conversationFlow.modelChoice.type` | string | yes | Type of model choice Allowed values: cascading. |
| `agentOverride.conversationFlow.modelChoice.model` | string | yes | Available LLM models for agents. |
| `agentOverride.conversationFlow.modelChoice.highPriority` | boolean | no | Whether to use high priority pool with more dedicated resource, default false |
| `agentOverride.conversationFlow.modelTemperature` | number | no | Controls the randomness of the model's responses. Lower values make responses more deterministic. |
| `agentOverride.conversationFlow.toolCallStrictMode` | boolean | no | Whether to use strict mode for tool calls. Only applicable when using certain supported models. |
| `agentOverride.conversationFlow.knowledgeBaseIds[]` | array<string> | no | Knowledge base IDs for RAG (Retrieval-Augmented Generation). |
| `agentOverride.conversationFlow.knowledgeBaseIds[]` | array<string> | no | Knowledge base IDs for RAG (Retrieval-Augmented Generation). |
| `agentOverride.conversationFlow.kbConfig` | object | no |  |
| `agentOverride.conversationFlow.kbConfig.topK` | number | no | Max number of knowledge base chunks to retrieve |
| `agentOverride.conversationFlow.kbConfig.filterScore` | number | no | Similarity threshold for filtering search results |
| `agentOverride.conversationFlow.startSpeaker` | string | no | Who starts the conversation - user or agent. Allowed values: user, agent. |
| `agentOverride.conversationFlow.beginAfterUserSilenceMs` | number | no | If set, the AI will begin the conversation after waiting for the user for the duration (in milliseconds) specified by this attribute. This only applies if the agent is configured to wait for the user to speak first. If not set, the agent will wait indefinitely for the user to speak. |
| `metadata` | object | no | An arbitrary object for storage purpose only. You can put anything here like your internal customer id associated with the call. Not used for processing. You can later get this field from the call object. |
| `retellLlmDynamicVariables` | object | no | Add optional dynamic variables in key value pairs of string that injects into your Response Engine prompt and tool description. Only applicable for Response Engine. |
| `customSipHeaders` | object | no | Add optional custom SIP headers to the call. |
| `ignoreE164Validation` | boolean | no | If true, the e.164 validation will be ignored for the from_number. This can be useful when you want to dial to internal pseudo numbers. This only applies when you are using custom telephony and does not apply when you are using Retell Telephony. If omitted, the default value is false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "agentName": "Ava Chen",
      "agentVersion": 1,
      "callAnalysis": {
        "callSuccessful": true,
        "callSummary": "string",
        "customAnalysisData": {},
        "inVoicemail": true,
        "userSentiment": "string"
      },
      "callCost": {
        "combinedCost": 1,
        "productCosts": [
          {
            "cost": 1,
            "isTransferLegCost": true,
            "product": "string",
            "unitPrice": 1
          }
        ],
        "totalDurationSeconds": 1,
        "totalDurationUnitPrice": 1
      },
      "callId": "string",
      "callStatus": "string",
      "callType": "string",
      "collectedDynamicVariables": {},
      "customSipHeaders": {},
      "dataStorageSetting": "string",
      "direction": "string",
      "disconnectionReason": "string",
      "durationMs": 1,
      "endTimestamp": 1,
      "fromNumber": "string",
      "knowledgeBaseRetrievedContentsUrl": "https://example.com",
      "latency": {
        "asr": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "e2e": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "knowledgeBase": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "llm": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "llmWebsocketNetworkRtt": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "s2s": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        },
        "tts": {
          "max": 1,
          "min": 1,
          "num": 1,
          "p50": 1,
          "p90": 1,
          "p95": 1,
          "p99": 1,
          "values": [
            1
          ]
        }
      },
      "llmTokenUsage": {
        "average": 1,
        "numRequests": 1,
        "values": [
          1
        ]
      },
      "metadata": {},
      "optInSignedUrl": true,
      "publicLogUrl": "https://example.com",
      "recordingMultiChannelUrl": "https://example.com",
      "recordingUrl": "https://example.com",
      "retellLlmDynamicVariables": {},
      "scrubbedRecordingMultiChannelUrl": "https://example.com",
      "scrubbedRecordingUrl": "https://example.com",
      "scrubbedTranscriptWithToolCalls": [
        {
          "content": "string",
          "role": "string",
          "words": [
            {
              "end": 1,
              "start": 1,
              "word": "string"
            }
          ]
        }
      ],
      "startTimestamp": 1,
      "telephonyIdentifier": {
        "twilioCallSid": "string"
      },
      "toNumber": "string",
      "transcript": "string",
      "transcriptObject": [
        {
          "content": "string",
          "role": "string",
          "words": [
            {
              "end": 1,
              "start": 1,
              "word": "string"
            }
          ]
        }
      ],
      "transcriptWithToolCalls": [
        {
          "content": "string",
          "role": "string",
          "words": [
            {
              "end": 1,
              "start": 1,
              "word": "string"
            }
          ]
        }
      ],
      "transferDestination": "string",
      "transferEndTimestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Corresponding agent id of this call. |
| `agentName` | string | Name of the agent. |
| `agentVersion` | number | The version of the agent. |
| `callAnalysis` | object |  |
| `callAnalysis.callSuccessful` | boolean | Whether the agent seems to have a successful call with the user, where the agent finishes the task, and the call was complete without being cutoff. |
| `callAnalysis.callSummary` | string | A high level summary of the call. |
| `callAnalysis.customAnalysisData` | object | Custom analysis data that was extracted based on the schema defined in agent post call analysis data. Can be empty if nothing is specified. |
| `callAnalysis.inVoicemail` | boolean | Whether the call is entered voicemail. |
| `callAnalysis.userSentiment` | string | Sentiment of the user in the call. Allowed values: Negative, Positive, Neutral, Unknown. |
| `callCost` | object | Cost of the call, including all the products and their costs and discount. |
| `callCost.combinedCost` | number | Combined cost of all individual costs in cents |
| `callCost.productCosts` | array<object> | List of products with their unit prices and costs in cents |
| `callCost.productCosts[].cost` | number | Cost for the product in cents for the duration of the call. |
| `callCost.productCosts[].isTransferLegCost` | boolean | True if this cost item is for a transfer segment. |
| `callCost.productCosts[].product` | string | Product name that has a cost associated with it. |
| `callCost.productCosts[].unitPrice` | number | Unit price of the product in cents per second. |
| `callCost.totalDurationSeconds` | number | Total duration of the call in seconds |
| `callCost.totalDurationUnitPrice` | number | Total unit duration price of all products in cents per second |
| `callId` | string | Unique id of the call. Used to identify the call in the LLM websocket and used to authenticate in the audio websocket. |
| `callStatus` | string | Status of call.  - `registered`: Call id issued, starting to make a call using this id. - `ongoing`: Call connected and ongoing. - `ended`: The underlying websocket has ended for the call. Either user or agent hung up, or call transferred. - `error`: Call encountered error. Allowed values: registered, not_connected, ongoing, ended, error. |
| `callType` | string | Type of the call. Used to distinguish between web call and phone call. Allowed values: phone_call. |
| `collectedDynamicVariables` | object | Dynamic variables collected from the call. Only available after the call ends. |
| `customSipHeaders` | object | Custom SIP headers to be added to the call. |
| `dataStorageSetting` | string | Data storage setting for this call's agent. "everything" stores all data, "everything_except_pii" excludes PII when possible, "basic_attributes_only" stores only metadata. Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `direction` | string | Direction of the phone call. Allowed values: inbound, outbound. |
| `disconnectionReason` | string |  |
| `durationMs` | number | Duration of the call in milliseconds. Available after call ends. |
| `endTimestamp` | number | End timestamp (milliseconds since epoch) of the call. Available after call ends. |
| `fromNumber` | string | The caller number. |
| `knowledgeBaseRetrievedContentsUrl` | string | URL to the knowledge base retrieved contents of the call. Available after call ends if the call utilizes knowledge base feature. It consists of the respond id and the retrieved contents related to that response. It's already rendered in call history tab of dashboard, and you can also manually download and check against the transcript to view the knowledge base retrieval results. |
| `latency` | object | Latency tracking of the call, available after call ends. Not all fields here will be available, as it depends on the type of call and feature used. |
| `latency.asr` | object |  |
| `latency.asr.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.asr.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.asr.num` | number | Number of data points (number of times latency is tracked). |
| `latency.asr.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.asr.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.asr.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.asr.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.asr.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.e2e` | object |  |
| `latency.e2e.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.e2e.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.e2e.num` | number | Number of data points (number of times latency is tracked). |
| `latency.e2e.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.e2e.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.e2e.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.e2e.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.e2e.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.knowledgeBase` | object |  |
| `latency.knowledgeBase.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.knowledgeBase.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.knowledgeBase.num` | number | Number of data points (number of times latency is tracked). |
| `latency.knowledgeBase.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.knowledgeBase.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.llm` | object |  |
| `latency.llm.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.llm.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.llm.num` | number | Number of data points (number of times latency is tracked). |
| `latency.llm.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.llm.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.llm.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.llm.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.llm.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt` | object |  |
| `latency.llmWebsocketNetworkRtt.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.num` | number | Number of data points (number of times latency is tracked). |
| `latency.llmWebsocketNetworkRtt.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.llmWebsocketNetworkRtt.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.s2s` | object |  |
| `latency.s2s.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.s2s.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.s2s.num` | number | Number of data points (number of times latency is tracked). |
| `latency.s2s.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.s2s.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.s2s.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.s2s.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.s2s.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `latency.tts` | object |  |
| `latency.tts.max` | number | Maximum latency in the call, measured in milliseconds. |
| `latency.tts.min` | number | Minimum latency in the call, measured in milliseconds. |
| `latency.tts.num` | number | Number of data points (number of times latency is tracked). |
| `latency.tts.p50` | number | 50 percentile of latency, measured in milliseconds. |
| `latency.tts.p90` | number | 90 percentile of latency, measured in milliseconds. |
| `latency.tts.p95` | number | 95 percentile of latency, measured in milliseconds. |
| `latency.tts.p99` | number | 99 percentile of latency, measured in milliseconds. |
| `latency.tts.values` | array<number> | All the latency data points in the call, measured in milliseconds. |
| `llmTokenUsage` | object | LLM token usage of the call, available after call ends. Not populated if using custom LLM, realtime API, or no LLM call is made. |
| `llmTokenUsage.average` | number | Average token count of the call. |
| `llmTokenUsage.numRequests` | number | Number of requests made to the LLM. |
| `llmTokenUsage.values` | array<number> | All the token count values in the call. |
| `metadata` | object | An arbitrary object for storage purpose only. You can put anything here like your internal customer id associated with the call. Not used for processing. You can later get this field from the call object. |
| `optInSignedUrl` | boolean | Whether this agent opts in for signed URLs for public logs and recordings. When enabled, the generated URLs will include security signatures that restrict access and automatically expire after 24 hours. |
| `publicLogUrl` | string | Public log of the call, containing details about all the requests and responses received in LLM WebSocket, latency tracking for each turntaking, helpful for debugging and tracing. Available after call ends. |
| `recordingMultiChannelUrl` | string | Recording of the call, with each party's audio stored in a separate channel. Available after the call ends. |
| `recordingUrl` | string | Recording of the call. Available after call ends. |
| `retellLlmDynamicVariables` | object | Add optional dynamic variables in key value pairs of string that injects into your Response Engine prompt and tool description. Only applicable for Response Engine. |
| `scrubbedRecordingMultiChannelUrl` | string | Recording of the call without PII, with each party's audio stored in a separate channel. Available after the call ends. |
| `scrubbedRecordingUrl` | string | Recording of the call without PII. Available after call ends. |
| `scrubbedTranscriptWithToolCalls` | array<object> | Transcript of the call weaved with tool call invocation and results, without PII. It precisely captures when (at what utterance, which word) the tool was invoked and what was the result. Available after call ends. |
| `scrubbedTranscriptWithToolCalls[].content` | string | Transcript of the utterances. |
| `scrubbedTranscriptWithToolCalls[].role` | string | Documents whether this utterance is spoken by agent or user. Allowed values: agent, user, transfer_target. |
| `scrubbedTranscriptWithToolCalls[].words` | array<object> | Array of words in the utterance with the word timestamp. Useful for understanding what word was spoken at what time. Note that the word timestamp is not guaranteed to be accurate, it's more like an approximation. |
| `scrubbedTranscriptWithToolCalls[].words[].end` | number | End time of the word in the call in second. This is relative audio time, not wall time. |
| `scrubbedTranscriptWithToolCalls[].words[].start` | number | Start time of the word in the call in second. This is relative audio time, not wall time. |
| `scrubbedTranscriptWithToolCalls[].words[].word` | string | Word transcript (with punctuation if applicable). |
| `startTimestamp` | number | Begin timestamp (milliseconds since epoch) of the call. Available after call starts. |
| `telephonyIdentifier` | object | Telephony identifier of the call, populated when available. Tracking purposes only. |
| `telephonyIdentifier.twilioCallSid` | string | Twilio call sid. |
| `toNumber` | string | The callee number. |
| `transcript` | string | Transcription of the call. Available after call ends. |
| `transcriptObject` | array<object> | Transcript of the call in the format of a list of utterance, with timestamp. Available after call ends. |
| `transcriptObject[].content` | string | Transcript of the utterances. |
| `transcriptObject[].role` | string | Documents whether this utterance is spoken by agent or user. Allowed values: agent, user, transfer_target. |
| `transcriptObject[].words` | array<object> | Array of words in the utterance with the word timestamp. Useful for understanding what word was spoken at what time. Note that the word timestamp is not guaranteed to be accurate, it's more like an approximation. |
| `transcriptObject[].words[].end` | number | End time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptObject[].words[].start` | number | Start time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptObject[].words[].word` | string | Word transcript (with punctuation if applicable). |
| `transcriptWithToolCalls` | array<object> | Transcript of the call weaved with tool call invocation and results. It precisely captures when (at what utterance, which word) the tool was invoked and what was the result. Available after call ends. |
| `transcriptWithToolCalls[].content` | string | Transcript of the utterances. |
| `transcriptWithToolCalls[].role` | string | Documents whether this utterance is spoken by agent or user. Allowed values: agent, user, transfer_target. |
| `transcriptWithToolCalls[].words` | array<object> | Array of words in the utterance with the word timestamp. Useful for understanding what word was spoken at what time. Note that the word timestamp is not guaranteed to be accurate, it's more like an approximation. |
| `transcriptWithToolCalls[].words[].end` | number | End time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptWithToolCalls[].words[].start` | number | Start time of the word in the call in second. This is relative audio time, not wall time. |
| `transcriptWithToolCalls[].words[].word` | string | Word transcript (with punctuation if applicable). |
| `transferDestination` | string | The destination number or identifier where the call was transferred to. Only populated when the disconnection reason was `call_transfer`. Can be a phone number or a SIP URI. SIP URIs are prefixed with "sip:" and may include a ";transport=..." portion (if transport is known) where the transport type can be "tls", "tcp" or "udp". |
| `transferEndTimestamp` | number | Transfer end timestamp (milliseconds since epoch) of the call. Available after transfer call ends. |

## Native endpoint

Through the native Retell AI API, this operation is `POST /v2/create-phone-call` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-phone-call.md) for the provider-specific parameters and requirements.

