# AssemblyAI: Transcribe Audio

Creates a new transcript from a media URL in AssemblyAI.

```
POST https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/transcribe-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/transcribe-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUrl": "https://example.com",
  "speechModels[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/transcribe-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUrl": "https://example.com",
    "speechModels[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | yes | Publicly reachable audio or video URL to transcribe. |
| `prompt` | string | no | Contextual prompt text to guide the transcription model. |
| `speechModels[]` | array<string> | yes | Preferred speech models in priority order. |
| `languageCode` | string | no | Language code for the audio when you want to force a specific language. |
| `languageDetection` | boolean | no | Detect the language automatically. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCodes[]` | array<string> | no | Language codes for code-switching audio. |
| `languageDetectionOptions` | object | no | Options for automatic language detection. |
| `punctuate` | boolean | no | Add punctuation to the transcript output. Default: `true`. |
| `formatText` | boolean | no | Apply text formatting to the transcript output. Default: `true`. |
| `multichannel` | boolean | no | Enable multichannel transcription for multi-track audio. |
| `speakerLabels` | boolean | no | Enable speaker diarization. |
| `speakerOptions` | object | no | Options for speaker diarization range handling. |
| `speakersExpected` | number | no | Expected number of speakers for diarization. |
| `audioStartFrom` | number | no | Start transcribing from this millisecond offset. |
| `audioEndAt` | number | no | Stop transcribing at this millisecond offset. |
| `autoHighlights` | boolean | no | Extract key phrases from the transcript. |
| `sentimentAnalysis` | boolean | no | Analyze sentiment across the transcript. |
| `entityDetection` | boolean | no | Detect entities in the transcript. |
| `contentSafety` | boolean | no | Run content moderation on the transcript. |
| `contentSafetyConfidence` | number | no | Confidence threshold for the content safety model. |
| `iabCategories` | boolean | no | Enable topic detection categories. |
| `redactPii` | boolean | no | Redact personally identifiable information in transcript text. |
| `redactPiiPolicies[]` | array<string> | no | PII policy list to enable during redaction. |
| `redactPiiSub` | string | no | Replacement logic for detected PII. |
| `redactPiiAudio` | boolean | no | Generate redacted audio with spoken PII beeped out. |
| `redactPiiAudioOptions` | object | no | Options for PII-redacted audio output. |
| `redactPiiAudioQuality` | string | no | Output file type for redacted audio. |
| `filterProfanity` | boolean | no | Filter profanity from transcript text. |
| `removeAudioTags` | string | no | Remove audio-event tags from transcript text on supported models. |
| `disfluencies` | boolean | no | Include filler words like um and uh in the transcript. |
| `customSpelling[]` | array<object> | no | Custom spelling and formatting rules using to/from values. |
| `keytermsPrompt[]` | array<string> | no | Domain-specific words or phrases to improve recognition. |
| `speechUnderstanding` | object | no | Speech-understanding tasks such as translation, speaker identification, or custom formatting. |
| `autoChapters` | boolean | no | Deprecated auto-chapters toggle. Default: `false`. |
| `summarization` | boolean | no | Deprecated summarization toggle. Default: `false`. |
| `summaryModel` | string | no | Deprecated summarization model option. |
| `summaryType` | string | no | Deprecated summary output type. |
| `webhookUrl` | string | no | Webhook URL to receive transcript completion events. |
| `webhookAuthHeaderName` | string | no | Webhook auth header name for completed or failed webhook deliveries. |
| `webhookAuthHeaderValue` | string | no | Webhook auth header value for completed or failed webhook deliveries. |
| `speechThreshold` | number | no | Minimum fraction of speech required in the audio. |
| `temperature` | number | no | Control randomness in model output. |
| `languageConfidenceThreshold` | number | no | Minimum confidence score required when automatic language detection is enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acousticModel": "string",
      "audioDuration": {},
      "audioEndAt": {},
      "audioStartFrom": {},
      "audioUrl": "https://example.com",
      "autoChapters": true,
      "autoHighlights": true,
      "autoHighlightsResult": {},
      "boostParam": {},
      "chapters": {},
      "confidence": {},
      "contentSafety": true,
      "contentSafetyLabels": {},
      "customSpelling": {},
      "customTopics": true,
      "customTopicsResults": {},
      "disfluencies": true,
      "entities": {},
      "entityDetection": true,
      "filterProfanity": true,
      "formatText": true,
      "iabCategories": true,
      "iabCategoriesResult": {},
      "id": "string",
      "isDeleted": {},
      "keytermsPrompt": {},
      "languageCode": "string",
      "languageConfidence": {},
      "languageConfidenceThreshold": {},
      "languageDetection": true,
      "languageDetectionOptions": {},
      "languageDetectionResults": {},
      "languageModel": "string",
      "multichannel": {},
      "projectId": 1,
      "prompt": {},
      "punctuate": true,
      "redactPii": true,
      "redactPiiAudio": true,
      "redactPiiAudioOptions": {},
      "redactPiiAudioQuality": "string",
      "redactPiiPolicies": [
        [
          "string"
        ]
      ],
      "redactPiiSub": "string",
      "removeAudioTags": {},
      "sentimentAnalysis": true,
      "sentimentAnalysisResults": {},
      "speakerLabels": true,
      "speakerOptions": {},
      "speakersExpected": {},
      "speechModel": {},
      "speechModels": [
        [
          "string"
        ]
      ],
      "speechModelUsed": {},
      "speechThreshold": {},
      "speechUnderstanding": {},
      "speedBoost": true,
      "status": "string",
      "summarization": true,
      "summary": {},
      "summaryModel": {},
      "summaryType": {},
      "temperature": {},
      "text": {},
      "throttled": true,
      "tokenId": 1,
      "topics": [
        [
          "string"
        ]
      ],
      "translatedTexts": {},
      "utterances": {},
      "webhookAuth": true,
      "webhookAuthHeaderName": {},
      "webhookStatusCode": {},
      "webhookUrl": {},
      "wordBoost": [
        [
          "string"
        ]
      ],
      "words": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acousticModel` | string |  |
| `audioDuration` | object |  |
| `audioEndAt` | object |  |
| `audioStartFrom` | object |  |
| `audioUrl` | string |  |
| `autoChapters` | boolean |  |
| `autoHighlights` | boolean |  |
| `autoHighlightsResult` | object |  |
| `boostParam` | object |  |
| `chapters` | object |  |
| `confidence` | object |  |
| `contentSafety` | boolean |  |
| `contentSafetyLabels` | object |  |
| `customSpelling` | object |  |
| `customTopics` | boolean |  |
| `customTopicsResults` | object |  |
| `disfluencies` | boolean |  |
| `entities` | object |  |
| `entityDetection` | boolean |  |
| `filterProfanity` | boolean |  |
| `formatText` | boolean |  |
| `iabCategories` | boolean |  |
| `iabCategoriesResult` | object |  |
| `id` | string |  |
| `isDeleted` | object |  |
| `keytermsPrompt` | object |  |
| `languageCode` | string |  |
| `languageConfidence` | object |  |
| `languageConfidenceThreshold` | object |  |
| `languageDetection` | boolean |  |
| `languageDetectionOptions` | object |  |
| `languageDetectionResults` | object |  |
| `languageModel` | string |  |
| `multichannel` | object |  |
| `projectId` | number |  |
| `prompt` | object |  |
| `punctuate` | boolean |  |
| `redactPii` | boolean |  |
| `redactPiiAudio` | boolean |  |
| `redactPiiAudioOptions` | object |  |
| `redactPiiAudioQuality` | string |  |
| `redactPiiPolicies[]` | array<string> |  |
| `redactPiiSub` | string |  |
| `removeAudioTags` | object |  |
| `sentimentAnalysis` | boolean |  |
| `sentimentAnalysisResults` | object |  |
| `speakerLabels` | boolean |  |
| `speakerOptions` | object |  |
| `speakersExpected` | object |  |
| `speechModel` | object |  |
| `speechModels[]` | array<string> |  |
| `speechModelUsed` | object |  |
| `speechThreshold` | object |  |
| `speechUnderstanding` | object |  |
| `speedBoost` | boolean |  |
| `status` | string |  |
| `summarization` | boolean |  |
| `summary` | object |  |
| `summaryModel` | object |  |
| `summaryType` | object |  |
| `temperature` | object |  |
| `text` | object |  |
| `throttled` | boolean |  |
| `tokenId` | number |  |
| `topics[]` | array<string> |  |
| `translatedTexts` | object |  |
| `utterances` | object |  |
| `webhookAuth` | boolean |  |
| `webhookAuthHeaderName` | object |  |
| `webhookStatusCode` | object |  |
| `webhookUrl` | object |  |
| `wordBoost[]` | array<string> |  |
| `words` | object |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `POST /v2/transcript` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transcribe-audio.md) for the provider-specific parameters and requirements.

