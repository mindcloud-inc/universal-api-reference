# AssemblyAI: Delete Transcript

Deletes one transcript from your AssemblyAI account.

```
DELETE https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/delete-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/delete-transcript?connectionId=$CONNECTION_ID&transcriptId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/delete-transcript?${params}`, {
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
| `transcriptId` | string | yes | The transcript ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acousticModel": "string",
      "audioChannels": {},
      "audioDuration": 1,
      "audioEndAt": {},
      "audioStartFrom": {},
      "audioUrl": "https://example.com",
      "autoChapters": true,
      "autoHighlights": true,
      "autoHighlightsResult": {},
      "boostParam": {},
      "chapters": {},
      "clusterId": {},
      "confidence": {},
      "contentSafety": {},
      "contentSafetyLabels": {},
      "customSpelling": {},
      "customTopics": true,
      "customTopicsResults": {},
      "disfluencies": true,
      "domain": {},
      "domainOptions": {},
      "dualChannel": {},
      "entities": {},
      "entityDetection": true,
      "error": {},
      "filterProfanity": true,
      "formatText": true,
      "iabCategories": {},
      "iabCategoriesResult": {},
      "id": "string",
      "isDeleted": true,
      "keytermsPrompt": [
        [
          "string"
        ]
      ],
      "languageCode": {},
      "languageCodes": {},
      "languageConfidence": {},
      "languageConfidenceThreshold": {},
      "languageDetection": true,
      "languageDetectionOptions": {},
      "languageDetectionResults": {},
      "languageModel": "string",
      "metadata": {},
      "multichannel": {},
      "projectId": 1,
      "prompt": {},
      "punctuate": true,
      "redactPii": true,
      "redactPiiAudio": true,
      "redactPiiAudioOptions": {},
      "redactPiiAudioQuality": {},
      "redactPiiPolicies": {},
      "redactPiiSub": {},
      "removeAudioTags": {},
      "sentences": {},
      "sentimentAnalysis": true,
      "sentimentAnalysisResults": {},
      "speakerCount": {},
      "speakerLabels": true,
      "speakerOptions": {},
      "speakersExpected": {},
      "speechModel": {},
      "speechModels": {},
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
      "webhookUrl": "https://example.com",
      "wordBoost": {},
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
| `audioChannels` | object |  |
| `audioDuration` | number |  |
| `audioEndAt` | object |  |
| `audioStartFrom` | object |  |
| `audioUrl` | string |  |
| `autoChapters` | boolean |  |
| `autoHighlights` | boolean |  |
| `autoHighlightsResult` | object |  |
| `boostParam` | object |  |
| `chapters` | object |  |
| `clusterId` | object |  |
| `confidence` | object |  |
| `contentSafety` | object |  |
| `contentSafetyLabels` | object |  |
| `customSpelling` | object |  |
| `customTopics` | boolean |  |
| `customTopicsResults` | object |  |
| `disfluencies` | boolean |  |
| `domain` | object |  |
| `domainOptions` | object |  |
| `dualChannel` | object |  |
| `entities` | object |  |
| `entityDetection` | boolean |  |
| `error` | object |  |
| `filterProfanity` | boolean |  |
| `formatText` | boolean |  |
| `iabCategories` | object |  |
| `iabCategoriesResult` | object |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `keytermsPrompt[]` | array<string> |  |
| `languageCode` | object |  |
| `languageCodes` | object |  |
| `languageConfidence` | object |  |
| `languageConfidenceThreshold` | object |  |
| `languageDetection` | boolean |  |
| `languageDetectionOptions` | object |  |
| `languageDetectionResults` | object |  |
| `languageModel` | string |  |
| `metadata` | object |  |
| `multichannel` | object |  |
| `projectId` | number |  |
| `prompt` | object |  |
| `punctuate` | boolean |  |
| `redactPii` | boolean |  |
| `redactPiiAudio` | boolean |  |
| `redactPiiAudioOptions` | object |  |
| `redactPiiAudioQuality` | object |  |
| `redactPiiPolicies` | object |  |
| `redactPiiSub` | object |  |
| `removeAudioTags` | object |  |
| `sentences` | object |  |
| `sentimentAnalysis` | boolean |  |
| `sentimentAnalysisResults` | object |  |
| `speakerCount` | object |  |
| `speakerLabels` | boolean |  |
| `speakerOptions` | object |  |
| `speakersExpected` | object |  |
| `speechModel` | object |  |
| `speechModels` | object |  |
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
| `text` | string |  |
| `throttled` | boolean |  |
| `tokenId` | number |  |
| `topics[]` | array<string> |  |
| `translatedTexts` | object |  |
| `utterances` | object |  |
| `webhookAuth` | boolean |  |
| `webhookAuthHeaderName` | object |  |
| `webhookStatusCode` | object |  |
| `webhookUrl` | string |  |
| `wordBoost` | object |  |
| `words` | object |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `DELETE /v2/transcript/:transcript_id` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-transcript.md) for the provider-specific parameters and requirements.

