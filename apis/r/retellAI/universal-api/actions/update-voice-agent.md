# Retell AI: Update Voice Agent

Updates a voice agent in Retell AI.

```
PUT https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-voice-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-voice-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "piiConfig.categories[]": [
    "string"
  ],
  "responseEngine.type": "string",
  "responseEngine.llmId": "string",
  "pronunciationDictionary[].word": "string",
  "pronunciationDictionary[].alphabet": "string",
  "pronunciationDictionary[].phoneme": "string",
  "voicemailOption.action": {},
  "voicemailOption.action.type": "ava@example.com",
  "voicemailOption.action.text": "ava@example.com",
  "ivrOption.action": {},
  "ivrOption.action.type": "string",
  "postCallAnalysisData[].type": "string",
  "postCallAnalysisData[].name": "Ava Chen",
  "postCallAnalysisData[].description": "string",
  "customSttConfig.provider": "string",
  "customSttConfig.endpointingMs": 1,
  "piiConfig.mode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-voice-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "piiConfig.categories[]": ["string"],
    "responseEngine.type": "string",
    "responseEngine.llmId": "string",
    "pronunciationDictionary[].word": "string",
    "pronunciationDictionary[].alphabet": "string",
    "pronunciationDictionary[].phoneme": "string",
    "voicemailOption.action": {},
    "voicemailOption.action.type": "ava@example.com",
    "voicemailOption.action.text": "ava@example.com",
    "ivrOption.action": {},
    "ivrOption.action.type": "string",
    "postCallAnalysisData[].type": "string",
    "postCallAnalysisData[].name": "Ava Chen",
    "postCallAnalysisData[].description": "string",
    "customSttConfig.provider": "string",
    "customSttConfig.endpointingMs": 1,
    "piiConfig.mode": "string",
    "piiConfig.categories[]": ["string"],
    "piiConfig.categories[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `backchannelWords[]` | array<string> | no | Only applicable when enable_backchannel is true. A list of words that the agent would use as backchannel. If not set, default backchannel words will apply. Check out [backchannel default words](/agent/interaction-configuration#backchannel) for more details. Note that certain voices do not work too well with certain words, so it's recommended to experiment before adding any words. |
| `boostedKeywords[]` | array<string> | no | Provide a customized list of keywords to bias the transcriber model, so that these words are more likely to get transcribed. Commonly used for names, brands, street, etc. |
| `fallbackVoiceIds[]` | array<string> | no | When TTS provider for the selected voice is experiencing outages, we would use fallback voices listed here for the agent. Voice id and the fallback voice ids must be from different TTS providers. The system would go through the list in order, if the first one in the list is also having outage, it would use the next one. Set to null to remove voice fallback for the agent. |
| `guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `postCallAnalysisData[]` | array<object> | no | Post call analysis data to extract from the call. This data will augment the pre-defined variables extracted in the call analysis. This will be available after the call ends. |
| `postCallAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `pronunciationDictionary[]` | array<object> | no | A list of words / phrases and their pronunciation to be used to guide the audio synthesize for consistent pronunciation. Check the dashboard to see what provider supports this feature. Set to null to remove pronunciation dictionary from this agent. |
| `webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to call_started, call_ended, call_analyzed. |
| `version` | number | no |  |
| `responseEngine` | object | no |  |
| `responseEngine.type` | string | yes | type of the Response Engine. Allowed values: retell-llm. |
| `responseEngine.llmId` | string | yes | id of the Retell LLM Response Engine. |
| `responseEngine.version` | number | no | Version of the Retell LLM Response Engine. |
| `agentName` | string | no | The name of the agent. Only used for your own reference. |
| `versionDescription` | string | no | Optional description of the agent version. Used for your own reference and documentation. |
| `voiceId` | string | no | Unique voice id used for the agent. Find list of available voices and their preview in Dashboard. |
| `voiceModel` | string | no | Select the voice model used for the selected voice. Each provider has a set of available voice models. Set to null to remove voice model selection, and default ones will apply. Check out dashboard for more details of each voice model. |
| `fallbackVoiceIds[]` | array<string> | no | When TTS provider for the selected voice is experiencing outages, we would use fallback voices listed here for the agent. Voice id and the fallback voice ids must be from different TTS providers. The system would go through the list in order, if the first one in the list is also having outage, it would use the next one. Set to null to remove voice fallback for the agent. |
| `fallbackVoiceIds[]` | array<string> | no | When TTS provider for the selected voice is experiencing outages, we would use fallback voices listed here for the agent. Voice id and the fallback voice ids must be from different TTS providers. The system would go through the list in order, if the first one in the list is also having outage, it would use the next one. Set to null to remove voice fallback for the agent. |
| `voiceTemperature` | number | no | Controls how stable the voice is. Value ranging from [0,2]. Lower value means more stable, and higher value means more variant speech generation. Check the dashboard to see what provider supports this feature. If unset, default value 1 will apply. |
| `voiceSpeed` | number | no | Controls speed of voice. Value ranging from [0.5,2]. Lower value means slower speech, while higher value means faster speech rate. If unset, default value 1 will apply. |
| `enableDynamicVoiceSpeed` | boolean | no | If set to true, will enable dynamic voice speed adjustment based on the user's speech rate and conversation context. If unset, default value false will apply. |
| `enableDynamicResponsiveness` | boolean | no | If set to true, the agent will dynamically adjust how quickly it responds based on the user's speech rate and past turn-taking behavior in the call. If unset, default value false will apply. |
| `volume` | number | no | If set, will control the volume of the agent. Value ranging from [0,2]. Lower value means quieter agent speech, while higher value means louder agent speech. If unset, default value 1 will apply. |
| `voiceEmotion` | string | no | Controls the emotional tone of the agent's voice. Currently supported for Cartesia and Minimax TTS providers. If unset, no emotion will be used. Allowed values: calm, sympathetic, happy, sad, angry, fearful, surprised. |
| `responsiveness` | number | no | Controls how responsive is the agent. Value ranging from [0,1]. Lower value means less responsive agent (wait more, respond slower), while higher value means faster exchanges (respond when it can). If unset, default value 1 will apply. |
| `interruptionSensitivity` | number | no | Controls how sensitive the agent is to user interruptions. Value ranging from [0,1]. Lower value means it will take longer / more words for user to interrupt agent, while higher value means it's easier for user to interrupt agent. If unset, default value 1 will apply. When this is set to 0, agent would never be interrupted. |
| `enableBackchannel` | boolean | no | Controls whether the agent would backchannel (agent interjects the speaker with phrases like "yeah", "uh-huh" to signify interest and engagement). Backchannel when enabled tends to show up more in longer user utterances. If not set, agent will not backchannel. |
| `backchannelFrequency` | number | no | Only applicable when enable_backchannel is true. Controls how often the agent would backchannel when a backchannel is possible. Value ranging from [0,1]. Lower value means less frequent backchannel, while higher value means more frequent backchannel. If unset, default value 0.8 will apply. |
| `backchannelWords[]` | array<string> | no | Only applicable when enable_backchannel is true. A list of words that the agent would use as backchannel. If not set, default backchannel words will apply. Check out [backchannel default words](/agent/interaction-configuration#backchannel) for more details. Note that certain voices do not work too well with certain words, so it's recommended to experiment before adding any words. |
| `backchannelWords[]` | array<string> | no | Only applicable when enable_backchannel is true. A list of words that the agent would use as backchannel. If not set, default backchannel words will apply. Check out [backchannel default words](/agent/interaction-configuration#backchannel) for more details. Note that certain voices do not work too well with certain words, so it's recommended to experiment before adding any words. |
| `reminderTriggerMs` | number | no | If set (in milliseconds), will trigger a reminder to the agent to speak if the user has been silent for the specified duration after some agent speech. Must be a positive number. If unset, default value of 10000 ms (10 s) will apply. |
| `reminderMaxCount` | number | no | If set, controls how many times agent would remind user when user is unresponsive. Must be a non negative integer. If unset, default value of 1 will apply (remind once). Set to 0 to disable agent from reminding. |
| `ambientSound` | string | no | If set, will add ambient environment sound to the call to make experience more realistic. Currently supports the following options: - `coffee-shop`: Coffee shop ambience with people chatting in background. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/coffee-shop.wav) - `convention-hall`: Convention hall ambience, with some echo and people chatting in background. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/convention-hall.wav) - `summer-outdoor`: Summer outdoor ambience with cicada chirping. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/summer-outdoor.wav) - `mountain-outdoor`: Mountain outdoor ambience with birds singing. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/mountain-outdoor.wav) - `static-noise`: Constant static noise. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/static-noise.wav) - `call-center`: Call center work noise. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/call-center.wav) Set to `null` to remove ambient sound from this agent. Allowed values: coffee-shop, convention-hall, summer-outdoor, mountain-outdoor, static-noise, call-center. |
| `ambientSoundVolume` | number | no | If set, will control the volume of the ambient sound. Value ranging from [0,2]. Lower value means quieter ambient sound, while higher value means louder ambient sound. If unset, default value 1 will apply. |
| `language` | string | no | Specifies what language (and dialect) the speech recognition will operate in. For instance, selecting `en-GB` optimizes speech recognition for British English. If unset, will use default value `en-US`. Select `multi` for multilingual support. |
| `webhookUrl` | string | no | The webhook for agent to listen to call events. See what events it would get at [webhook doc](/features/webhook). If set, will binds webhook events for this agent to the specified url, and will ignore the account level webhook for this agent. Set to `null` to remove webhook url from this agent. |
| `webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to call_started, call_ended, call_analyzed. |
| `webhookEvents[]` | array<string> | no | Which webhook events this agent should receive. If not set, defaults to call_started, call_ended, call_analyzed. |
| `webhookTimeoutMs` | number | no | The timeout for the webhook in milliseconds. If not set, default value of 10000 will apply. |
| `boostedKeywords[]` | array<string> | no | Provide a customized list of keywords to bias the transcriber model, so that these words are more likely to get transcribed. Commonly used for names, brands, street, etc. |
| `boostedKeywords[]` | array<string> | no | Provide a customized list of keywords to bias the transcriber model, so that these words are more likely to get transcribed. Commonly used for names, brands, street, etc. |
| `dataStorageSetting` | string | no | Granular setting to manage how Retell stores sensitive data (transcripts, recordings, logs, etc.). This replaces the deprecated `opt_out_sensitive_data_storage` field. - `everything`: Store all data including transcripts, recordings, and logs. - `everything_except_pii`: Store data without PII when PII is detected. - `basic_attributes_only`: Store only basic attributes; no transcripts/recordings/logs. If not set, default value of "everything" will apply. Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `dataStorageRetentionDays` | number | no | Number of days to retain call/chat data before automatic deletion. Must be between 1 and 730 days. If not set, data is retained forever (no automatic deletion). |
| `optInSignedUrl` | boolean | no | Whether this agent opts in for signed URLs for public logs and recordings. When enabled, the generated URLs will include security signatures that restrict access and automatically expire after 24 hours. |
| `signedUrlExpirationMs` | number | no | The expiration time for the signed url in milliseconds. Only applicable when opt_in_signed_url is true. If not set, default value of 86400000 (24 hours) will apply. |
| `pronunciationDictionary[]` | array<object> | no | A list of words / phrases and their pronunciation to be used to guide the audio synthesize for consistent pronunciation. Check the dashboard to see what provider supports this feature. Set to null to remove pronunciation dictionary from this agent. |
| `pronunciationDictionary[]` | array<object> | no | A list of words / phrases and their pronunciation to be used to guide the audio synthesize for consistent pronunciation. Check the dashboard to see what provider supports this feature. Set to null to remove pronunciation dictionary from this agent. |
| `pronunciationDictionary[].word` | string | yes | The string of word / phrase to be annotated with pronunciation. |
| `pronunciationDictionary[].alphabet` | string | yes | The phonetic alphabet to be used for pronunciation. Allowed values: ipa, cmu. |
| `pronunciationDictionary[].phoneme` | string | yes | Pronunciation of the word in the format of a IPA / CMU pronunciation. |
| `normalizeForSpeech` | boolean | no | If set to true, will normalize the some part of text (number, currency, date, etc) to spoken to its spoken form for more consistent speech synthesis (sometimes the voice synthesize system itself might read these wrong with the raw text). For example, it will convert "Call my number 2137112342 on Jul 5th, 2024 for the $24.12 payment" to "Call my number two one three seven one one two three four two on july fifth, twenty twenty four for the twenty four dollars twelve cents payment" before starting audio generation. |
| `endCallAfterSilenceMs` | number | no | If users stay silent for a period after agent speech, end the call. The minimum value allowed is 10,000 ms (10 s). By default, this is set to 600000 (10 min). |
| `maxCallDurationMs` | number | no | Maximum allowed length for the call, will force end the call if reached. The minimum value allowed is 60,000 ms (1 min), and maximum value allowed is 7,200,000 (2 hours). By default, this is set to 3,600,000 (1 hour). |
| `enableVoicemailDetection` | boolean | no | If set to true, will detect whether the call enters a voicemail. Note that this feature is only available for phone calls. |
| `voicemailMessage` | string | no | The message to be played when the call enters a voicemail. Note that this feature is only available for phone calls. If you want to hangup after hitting voicemail, set this to empty string. |
| `voicemailDetectionTimeoutMs` | number | no | Configures when to stop running voicemail detection, as it becomes unlikely to hit voicemail after a couple minutes, and keep running it will only have negative impact. The minimum value allowed is 5,000 ms (5 s), and maximum value allowed is 180,000 (3 minutes). By default, this is set to 30,000 (30 s). |
| `voicemailOption` | object | no | If this option is set, the call will try to detect voicemail in the first 3 minutes of the call. Actions defined (hangup, or leave a message) will be applied when the voicemail is detected. Set this to null to disable voicemail detection. |
| `voicemailOption.action` | object | yes |  |
| `voicemailOption.action.type` | string | yes | Allowed values: prompt. |
| `voicemailOption.action.text` | string | yes | The prompt used to generate the text to be spoken when the call is detected to be in voicemail. |
| `ivrOption` | object | no | If this option is set, the call will try to detect IVR in the first 3 minutes of the call. Actions defined will be applied when the IVR is detected. Set this to null to disable IVR detection. |
| `ivrOption.action` | object | yes |  |
| `ivrOption.action.type` | string | yes | Allowed values: hangup. |
| `postCallAnalysisData[]` | array<object> | no | Post call analysis data to extract from the call. This data will augment the pre-defined variables extracted in the call analysis. This will be available after the call ends. |
| `postCallAnalysisData[]` | array<object> | no | Post call analysis data to extract from the call. This data will augment the pre-defined variables extracted in the call analysis. This will be available after the call ends. |
| `postCallAnalysisData[].type` | string | yes | Type of the variable to extract. Allowed values: string. |
| `postCallAnalysisData[].name` | string | yes | Name of the variable. |
| `postCallAnalysisData[].description` | string | yes | Description of the variable. |
| `postCallAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `postCallAnalysisData[].examples[]` | array<string> | no | Examples of the variable value to teach model the style and syntax. |
| `postCallAnalysisData[].required` | boolean | no | Whether this data is required. If true and the data is not extracted, the call will be marked as unsuccessful. |
| `postCallAnalysisModel` | string | no | Available LLM models for agents. |
| `analysisSuccessfulPrompt` | string | no | Prompt to determine whether the post call or chat analysis should mark the interaction as successful. Set to null to use the default prompt. |
| `analysisSummaryPrompt` | string | no | Prompt to guide how the post call or chat analysis summary should be generated. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `analysisUserSentimentPrompt` | string | no | Prompt to guide how the post call or chat analysis should evaluate user sentiment. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `beginMessageDelayMs` | number | no | If set, will delay the first message by the specified amount of milliseconds, so that it gives user more time to prepare to take the call. Valid range is [0, 5000]. If not set or set to 0, agent will speak immediately. Only applicable when agent speaks first. |
| `ringDurationMs` | number | no | If set, the phone ringing will last for the specified amount of milliseconds. This applies for both outbound call ringtime, and call transfer ringtime. Default to 30000 (30 s). Valid range is [5000, 300000]. |
| `sttMode` | string | no | If set, determines whether speech to text should focus on latency or accuracy. Default to fast mode. When set to custom, custom_stt_config must be provided. Allowed values: fast, accurate, custom. |
| `customSttConfig` | object | no | Custom STT configuration. Only used when stt_mode is set to custom. |
| `customSttConfig.provider` | string | yes | The STT provider to use. Allowed values: azure, deepgram. |
| `customSttConfig.endpointingMs` | number | yes | Endpointing timeout in milliseconds. Minimum is 100 for azure, 10 for deepgram. |
| `vocabSpecialization` | string | no | If set, determines the vocabulary set to use for transcription. This setting only applies for English agents, for non English agent, this setting is a no-op. Default to general. Allowed values: general, medical. |
| `allowUserDtmf` | boolean | no | If set to true, DTMF input will be accepted and processed. If false, any DTMF input will be ignored. Default to true. |
| `userDtmfOptions` | object | no |  |
| `userDtmfOptions.digitLimit` | number | no | The maximum number of digits allowed in the user's DTMF (Dual-Tone Multi-Frequency) input per turn. Once this limit is reached, the input is considered complete and a response will be generated immediately. |
| `userDtmfOptions.terminationKey` | string | no | A single key that signals the end of DTMF input. Acceptable values include any digit (0-9), the pound/hash symbol (#), or the asterisk (*). |
| `userDtmfOptions.timeoutMs` | number | no | The time (in milliseconds) to wait for user DTMF input before timing out. The timer resets with each digit received. |
| `denoisingMode` | string | no | If set, determines what denoising mode to use. Use "no-denoise" to bypass all audio denoising. Default to noise-cancellation. Allowed values: no-denoise, noise-cancellation, noise-and-background-speech-cancellation. |
| `piiConfig` | object | no |  |
| `piiConfig.mode` | string | yes | The processing mode for PII scrubbing. Currently only post-call is supported. Allowed values: post_call. |
| `piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `piiConfig.categories[]` | array<string> | yes | List of PII categories to scrub from transcripts and recordings. |
| `guardrailConfig` | object | no |  |
| `guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `guardrailConfig.outputTopics[]` | array<string> | no | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrailConfig.inputTopics[]` | array<string> | no | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `isPublic` | boolean | no | Whether the agent is public. When set to true, the agent is available for public agent preview link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "agentName": "Ava Chen",
      "allowUserDtmf": true,
      "ambientSound": "string",
      "ambientSoundVolume": 1,
      "analysisSuccessfulPrompt": "string",
      "analysisSummaryPrompt": "string",
      "analysisUserSentimentPrompt": "string",
      "backchannelFrequency": 1,
      "backchannelWords": [
        "string"
      ],
      "beginMessageDelayMs": 1,
      "boostedKeywords": [
        "string"
      ],
      "customSttConfig": {
        "endpointingMs": 1,
        "provider": "string"
      },
      "dataStorageRetentionDays": 1,
      "dataStorageSetting": "string",
      "denoisingMode": "string",
      "enableBackchannel": true,
      "enableDynamicResponsiveness": true,
      "enableDynamicVoiceSpeed": true,
      "enableVoicemailDetection": true,
      "endCallAfterSilenceMs": 1,
      "fallbackVoiceIds": [
        "string"
      ],
      "guardrailConfig": {
        "inputTopics": [
          "string"
        ],
        "outputTopics": [
          "string"
        ]
      },
      "interruptionSensitivity": 1,
      "isPublic": true,
      "isPublished": true,
      "ivrOption": {
        "action": {
          "type": "string"
        }
      },
      "language": "string",
      "lastModificationTimestamp": 1,
      "maxCallDurationMs": 1,
      "normalizeForSpeech": true,
      "optInSignedUrl": true,
      "piiConfig": {
        "categories": [
          "string"
        ],
        "mode": "string"
      },
      "postCallAnalysisData": [
        {
          "description": "string",
          "examples": [
            "string"
          ],
          "name": "Ava Chen",
          "required": true,
          "type": "string"
        }
      ],
      "postCallAnalysisModel": "string",
      "pronunciationDictionary": [
        {
          "alphabet": "string",
          "phoneme": "string",
          "word": "string"
        }
      ],
      "reminderMaxCount": 1,
      "reminderTriggerMs": 1,
      "responseEngine": {
        "llmId": "string",
        "type": "string",
        "version": 1
      },
      "responsiveness": 1,
      "ringDurationMs": 1,
      "signedUrlExpirationMs": 1,
      "sttMode": "string",
      "userDtmfOptions": {
        "digitLimit": 1,
        "terminationKey": "string",
        "timeoutMs": 1
      },
      "version": 1,
      "versionDescription": "string",
      "vocabSpecialization": "string",
      "voiceEmotion": "string",
      "voiceId": "string",
      "voicemailDetectionTimeoutMs": 1,
      "voicemailMessage": "ava@example.com",
      "voicemailOption": {
        "action": {
          "text": "ava@example.com",
          "type": "ava@example.com"
        }
      },
      "voiceModel": "string",
      "voiceSpeed": 1,
      "voiceTemperature": 1,
      "volume": 1,
      "webhookEvents": [
        "string"
      ],
      "webhookTimeoutMs": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | Unique id of agent. |
| `agentName` | string | The name of the agent. Only used for your own reference. |
| `allowUserDtmf` | boolean | If set to true, DTMF input will be accepted and processed. If false, any DTMF input will be ignored. Default to true. |
| `ambientSound` | string | If set, will add ambient environment sound to the call to make experience more realistic. Currently supports the following options:  - `coffee-shop`: Coffee shop ambience with people chatting in background. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/coffee-shop.wav) - `convention-hall`: Convention hall ambience, with some echo and people chatting in background. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/convention-hall.wav) - `summer-outdoor`: Summer outdoor ambience with cicada chirping. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/summer-outdoor.wav) - `mountain-outdoor`: Mountain outdoor ambience with birds singing. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/mountain-outdoor.wav) - `static-noise`: Constant static noise. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/static-noise.wav) - `call-center`: Call center work noise. [Listen to Ambience](https://retell-utils-public.s3.us-west-2.amazonaws.com/call-center.wav) Set to `null` to remove ambient sound from this agent. Allowed values: coffee-shop, convention-hall, summer-outdoor, mountain-outdoor, static-noise, call-center. |
| `ambientSoundVolume` | number | If set, will control the volume of the ambient sound. Value ranging from [0,2]. Lower value means quieter ambient sound, while higher value means louder ambient sound. If unset, default value 1 will apply. |
| `analysisSuccessfulPrompt` | string | Prompt to determine whether the post call or chat analysis should mark the interaction as successful. Set to null to use the default prompt. |
| `analysisSummaryPrompt` | string | Prompt to guide how the post call or chat analysis summary should be generated. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `analysisUserSentimentPrompt` | string | Prompt to guide how the post call or chat analysis should evaluate user sentiment. When unset, the default system prompt is used. Set to null to use the default prompt. |
| `backchannelFrequency` | number | Only applicable when enable_backchannel is true. Controls how often the agent would backchannel when a backchannel is possible. Value ranging from [0,1]. Lower value means less frequent backchannel, while higher value means more frequent backchannel. If unset, default value 0.8 will apply. |
| `backchannelWords` | array<string> | Only applicable when enable_backchannel is true. A list of words that the agent would use as backchannel. If not set, default backchannel words will apply. Check out [backchannel default words](/agent/interaction-configuration#backchannel) for more details. Note that certain voices do not work too well with certain words, so it's recommended to experiment before adding any words. |
| `beginMessageDelayMs` | number | If set, will delay the first message by the specified amount of milliseconds, so that it gives user more time to prepare to take the call. Valid range is [0, 5000]. If not set or set to 0, agent will speak immediately. Only applicable when agent speaks first. |
| `boostedKeywords` | array<string> | Provide a customized list of keywords to bias the transcriber model, so that these words are more likely to get transcribed. Commonly used for names, brands, street, etc. |
| `customSttConfig` | object | Custom STT configuration. Only used when stt_mode is set to custom. |
| `customSttConfig.endpointingMs` | number | Endpointing timeout in milliseconds. Minimum is 100 for azure, 10 for deepgram. |
| `customSttConfig.provider` | string | The STT provider to use. Allowed values: azure, deepgram. |
| `dataStorageRetentionDays` | number | Number of days to retain call/chat data before automatic deletion. Must be between 1 and 730 days. If not set, data is retained forever (no automatic deletion). |
| `dataStorageSetting` | string | Granular setting to manage how Retell stores sensitive data (transcripts, recordings, logs, etc.). This replaces the deprecated `opt_out_sensitive_data_storage` field. - `everything`: Store all data including transcripts, recordings, and logs. - `everything_except_pii`: Store data without PII when PII is detected. - `basic_attributes_only`: Store only basic attributes; no transcripts/recordings/logs. If not set, default value of "everything" will apply. Allowed values: everything, everything_except_pii, basic_attributes_only. |
| `denoisingMode` | string | If set, determines what denoising mode to use. Use "no-denoise" to bypass all audio denoising. Default to noise-cancellation. Allowed values: no-denoise, noise-cancellation, noise-and-background-speech-cancellation. |
| `enableBackchannel` | boolean | Controls whether the agent would backchannel (agent interjects the speaker with phrases like "yeah", "uh-huh" to signify interest and engagement). Backchannel when enabled tends to show up more in longer user utterances. If not set, agent will not backchannel. |
| `enableDynamicResponsiveness` | boolean | If set to true, the agent will dynamically adjust how quickly it responds based on the user's speech rate and past turn-taking behavior in the call. If unset, default value false will apply. |
| `enableDynamicVoiceSpeed` | boolean | If set to true, will enable dynamic voice speed adjustment based on the user's speech rate and conversation context. If unset, default value false will apply. |
| `enableVoicemailDetection` | boolean | If set to true, will detect whether the call enters a voicemail. Note that this feature is only available for phone calls. |
| `endCallAfterSilenceMs` | number | If users stay silent for a period after agent speech, end the call. The minimum value allowed is 10,000 ms (10 s). By default, this is set to 600000 (10 min). |
| `fallbackVoiceIds` | array<string> | When TTS provider for the selected voice is experiencing outages, we would use fallback voices listed here for the agent. Voice id and the fallback voice ids must be from different TTS providers. The system would go through the list in order, if the first one in the list is also having outage, it would use the next one. Set to null to remove voice fallback for the agent. |
| `guardrailConfig` | object |  |
| `guardrailConfig.inputTopics` | array<string> | Selected prohibited user topic categories to check. When user messages contain these topics, the agent will respond with a placeholder message instead of processing the request. |
| `guardrailConfig.outputTopics` | array<string> | Selected prohibited agent topic categories to check. When agent messages contain these topics, they will be replaced with a placeholder message. |
| `interruptionSensitivity` | number | Controls how sensitive the agent is to user interruptions. Value ranging from [0,1]. Lower value means it will take longer / more words for user to interrupt agent, while higher value means it's easier for user to interrupt agent. If unset, default value 1 will apply. When this is set to 0, agent would never be interrupted. |
| `isPublic` | boolean | Whether the agent is public. When set to true, the agent is available for public agent preview link. |
| `isPublished` | boolean | Whether the agent is published. |
| `ivrOption` | object | If this option is set, the call will try to detect IVR in the first 3 minutes of the call. Actions defined will be applied when the IVR is detected. Set this to null to disable IVR detection. |
| `ivrOption.action` | object |  |
| `ivrOption.action.type` | string | Allowed values: hangup. |
| `language` | string | Specifies what language (and dialect) the speech recognition will operate in. For instance, selecting `en-GB` optimizes speech recognition for British English. If unset, will use default value `en-US`. Select `multi` for multilingual support. |
| `lastModificationTimestamp` | number | Last modification timestamp (milliseconds since epoch). Either the time of last update or creation if no updates available. |
| `maxCallDurationMs` | number | Maximum allowed length for the call, will force end the call if reached. The minimum value allowed is 60,000 ms (1 min), and maximum value allowed is 7,200,000 (2 hours). By default, this is set to 3,600,000 (1 hour). |
| `normalizeForSpeech` | boolean | If set to true, will normalize the some part of text (number, currency, date, etc) to spoken to its spoken form for more consistent speech synthesis (sometimes the voice synthesize system itself might read these wrong with the raw text). For example, it will convert "Call my number 2137112342 on Jul 5th, 2024 for the $24.12 payment" to "Call my number two one three seven one one two three four two on july fifth, twenty twenty four for the twenty four dollars twelve cents payment" before starting audio generation. |
| `optInSignedUrl` | boolean | Whether this agent opts in for signed URLs for public logs and recordings. When enabled, the generated URLs will include security signatures that restrict access and automatically expire after 24 hours. |
| `piiConfig` | object |  |
| `piiConfig.categories` | array<string> | List of PII categories to scrub from transcripts and recordings. |
| `piiConfig.mode` | string | The processing mode for PII scrubbing. Currently only post-call is supported. Allowed values: post_call. |
| `postCallAnalysisData` | array<object> | Post call analysis data to extract from the call. This data will augment the pre-defined variables extracted in the call analysis. This will be available after the call ends. |
| `postCallAnalysisData[].description` | string | Description of the variable. |
| `postCallAnalysisData[].examples` | array<string> | Examples of the variable value to teach model the style and syntax. |
| `postCallAnalysisData[].name` | string | Name of the variable. |
| `postCallAnalysisData[].required` | boolean | Whether this data is required. If true and the data is not extracted, the call will be marked as unsuccessful. |
| `postCallAnalysisData[].type` | string | Type of the variable to extract. Allowed values: string. |
| `postCallAnalysisModel` | string | Available LLM models for agents. |
| `pronunciationDictionary` | array<object> | A list of words / phrases and their pronunciation to be used to guide the audio synthesize for consistent pronunciation. Check the dashboard to see what provider supports this feature. Set to null to remove pronunciation dictionary from this agent. |
| `pronunciationDictionary[].alphabet` | string | The phonetic alphabet to be used for pronunciation. Allowed values: ipa, cmu. |
| `pronunciationDictionary[].phoneme` | string | Pronunciation of the word in the format of a IPA / CMU pronunciation. |
| `pronunciationDictionary[].word` | string | The string of word / phrase to be annotated with pronunciation. |
| `reminderMaxCount` | number | If set, controls how many times agent would remind user when user is unresponsive. Must be a non negative integer. If unset, default value of 1 will apply (remind once). Set to 0 to disable agent from reminding. |
| `reminderTriggerMs` | number | If set (in milliseconds), will trigger a reminder to the agent to speak if the user has been silent for the specified duration after some agent speech. Must be a positive number. If unset, default value of 10000 ms (10 s) will apply. |
| `responseEngine` | object |  |
| `responseEngine.llmId` | string | id of the Retell LLM Response Engine. |
| `responseEngine.type` | string | type of the Response Engine. Allowed values: retell-llm. |
| `responseEngine.version` | number | Version of the Retell LLM Response Engine. |
| `responsiveness` | number | Controls how responsive is the agent. Value ranging from [0,1]. Lower value means less responsive agent (wait more, respond slower), while higher value means faster exchanges (respond when it can). If unset, default value 1 will apply. |
| `ringDurationMs` | number | If set, the phone ringing will last for the specified amount of milliseconds. This applies for both outbound call ringtime, and call transfer ringtime. Default to 30000 (30 s). Valid range is [5000, 300000]. |
| `signedUrlExpirationMs` | number | The expiration time for the signed url in milliseconds. Only applicable when opt_in_signed_url is true. If not set, default value of 86400000 (24 hours) will apply. |
| `sttMode` | string | If set, determines whether speech to text should focus on latency or accuracy. Default to fast mode. When set to custom, custom_stt_config must be provided. Allowed values: fast, accurate, custom. |
| `userDtmfOptions` | object |  |
| `userDtmfOptions.digitLimit` | number | The maximum number of digits allowed in the user's DTMF (Dual-Tone Multi-Frequency) input per turn. Once this limit is reached, the input is considered complete and a response will be generated immediately. |
| `userDtmfOptions.terminationKey` | string | A single key that signals the end of DTMF input. Acceptable values include any digit (0-9), the pound/hash symbol (#), or the asterisk (*). |
| `userDtmfOptions.timeoutMs` | number | The time (in milliseconds) to wait for user DTMF input before timing out. The timer resets with each digit received. |
| `version` | number | Version of the agent. |
| `versionDescription` | string | Optional description of the agent version. Used for your own reference and documentation. |
| `vocabSpecialization` | string | If set, determines the vocabulary set to use for transcription. This setting only applies for English agents, for non English agent, this setting is a no-op. Default to general. Allowed values: general, medical. |
| `voiceEmotion` | string | Controls the emotional tone of the agent's voice. Currently supported for Cartesia and Minimax TTS providers. If unset, no emotion will be used. Allowed values: calm, sympathetic, happy, sad, angry, fearful, surprised. |
| `voiceId` | string | Unique voice id used for the agent. Find list of available voices and their preview in Dashboard. |
| `voicemailDetectionTimeoutMs` | number | Configures when to stop running voicemail detection, as it becomes unlikely to hit voicemail after a couple minutes, and keep running it will only have negative impact. The minimum value allowed is 5,000 ms (5 s), and maximum value allowed is 180,000 (3 minutes). By default, this is set to 30,000 (30 s). |
| `voicemailMessage` | string | The message to be played when the call enters a voicemail. Note that this feature is only available for phone calls. If you want to hangup after hitting voicemail, set this to empty string. |
| `voicemailOption` | object | If this option is set, the call will try to detect voicemail in the first 3 minutes of the call. Actions defined (hangup, or leave a message) will be applied when the voicemail is detected. Set this to null to disable voicemail detection. |
| `voicemailOption.action` | object |  |
| `voicemailOption.action.text` | string | The prompt used to generate the text to be spoken when the call is detected to be in voicemail. |
| `voicemailOption.action.type` | string | Allowed values: prompt. |
| `voiceModel` | string | Select the voice model used for the selected voice. Each provider has a set of available voice models. Set to null to remove voice model selection, and default ones will apply. Check out dashboard for more details of each voice model. |
| `voiceSpeed` | number | Controls speed of voice. Value ranging from [0.5,2]. Lower value means slower speech, while higher value means faster speech rate. If unset, default value 1 will apply. |
| `voiceTemperature` | number | Controls how stable the voice is. Value ranging from [0,2]. Lower value means more stable, and higher value means more variant speech generation. Check the dashboard to see what provider supports this feature. If unset, default value 1 will apply. |
| `volume` | number | If set, will control the volume of the agent. Value ranging from [0,2]. Lower value means quieter agent speech, while higher value means louder agent speech. If unset, default value 1 will apply. |
| `webhookEvents` | array<string> | Which webhook events this agent should receive. If not set, defaults to call_started, call_ended, call_analyzed. |
| `webhookTimeoutMs` | number | The timeout for the webhook in milliseconds. If not set, default value of 10000 will apply. |
| `webhookUrl` | string | The webhook for agent to listen to call events. See what events it would get at [webhook doc](/features/webhook). If set, will binds webhook events for this agent to the specified url, and will ignore the account level webhook for this agent. Set to `null` to remove webhook url from this agent. |

## Native endpoint

Through the native Retell AI API, this operation is `PATCH /update-agent/{agent_id}` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-voice-agent.md) for the provider-specific parameters and requirements.

