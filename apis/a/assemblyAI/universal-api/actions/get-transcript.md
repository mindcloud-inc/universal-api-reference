# AssemblyAI: Get Transcript

Retrieves one transcript from your AssemblyAI account.

```
GET https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript?connectionId=$CONNECTION_ID&transcriptId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript?${params}`, {
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
| `transcriptId` | string | yes | The transcript ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acousticModel": "string",
      "audioDuration": 1,
      "audioEndAt": {},
      "audioStartFrom": {},
      "audioUrl": "https://example.com",
      "autoChapters": true,
      "autoHighlights": true,
      "autoHighlightsResult": {},
      "boostParam": {},
      "chapters": {},
      "confidence": 1,
      "contentSafety": true,
      "contentSafetyLabels": {
        "results": [
          [
            "string"
          ]
        ],
        "status": "string",
        "summary": {}
      },
      "customSpelling": {},
      "customTopics": true,
      "customTopicsResults": {},
      "disfluencies": true,
      "entities": {},
      "entityDetection": true,
      "filterProfanity": true,
      "formatText": true,
      "iabCategories": true,
      "iabCategoriesResult": {
        "results": [
          [
            "string"
          ]
        ],
        "status": "string",
        "summary": {}
      },
      "id": "string",
      "isDeleted": {},
      "keytermsPrompt": [
        [
          "string"
        ]
      ],
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
      "speechModelUsed": "string",
      "speechThreshold": {},
      "speechUnderstanding": {},
      "speedBoost": true,
      "status": "string",
      "summarization": true,
      "summary": {},
      "summaryModel": {},
      "summaryType": {},
      "temperature": {},
      "text": "string",
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
      "words": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acousticModel` | string |  |
| `audioDuration` | number |  |
| `audioEndAt` | object |  |
| `audioStartFrom` | object |  |
| `audioUrl` | string |  |
| `autoChapters` | boolean |  |
| `autoHighlights` | boolean |  |
| `autoHighlightsResult` | object |  |
| `boostParam` | object |  |
| `chapters` | object |  |
| `confidence` | number |  |
| `contentSafety` | boolean |  |
| `contentSafetyLabels` | object |  |
| `contentSafetyLabels.results[]` | array<string> |  |
| `contentSafetyLabels.status` | string |  |
| `contentSafetyLabels.summary` | object |  |
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
| `iabCategoriesResult.results[]` | array<string> |  |
| `iabCategoriesResult.status` | string |  |
| `iabCategoriesResult.summary` | object |  |
| `id` | string |  |
| `isDeleted` | object |  |
| `keytermsPrompt[]` | array<string> |  |
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
| `speechModelUsed` | string |  |
| `speechThreshold` | object |  |
| `speechUnderstanding` | object |  |
| `speedBoost` | boolean |  |
| `status` | string |  |
| `summarization` | boolean |  |
| `summary` | object |  |
| `summaryModel` | object |  |
| `summaryType` | object |  |
| `temperature` | object |  |
| `text` | string |  |
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
| `words[]` | array<object> |  |
| `words[].confidence` | number |  |
| `words[].end` | number |  |
| `words[].speaker` | object |  |
| `words[].start` | number |  |
| `words[].text` | string |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `GET /v2/transcript/:transcript_id` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript.md) for the provider-specific parameters and requirements.

