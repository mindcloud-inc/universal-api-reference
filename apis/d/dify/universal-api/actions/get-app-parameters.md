# Dify: Get App Parameters

Retrieves application parameters from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-parameters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-parameters?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "annotationReply": {},
      "fileUpload": {},
      "moreLikeThis": {},
      "openingStatement": "string",
      "retrieverResource": {},
      "sensitiveWordAvoidance": {},
      "speechToText": {},
      "suggestedQuestions": [
        "string"
      ],
      "suggestedQuestionsAfterAnswer": {},
      "systemParameters": {},
      "textToSpeech": {},
      "userInputForm": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotationReply` | object |  |
| `fileUpload` | object |  |
| `moreLikeThis` | object |  |
| `openingStatement` | string |  |
| `retrieverResource` | object |  |
| `sensitiveWordAvoidance` | object |  |
| `speechToText` | object |  |
| `suggestedQuestions` | array<string> |  |
| `suggestedQuestionsAfterAnswer` | object |  |
| `systemParameters` | object |  |
| `textToSpeech` | object |  |
| `userInputForm` | array<object> |  |

## Native endpoint

Through the native Dify API, this operation is `GET /parameters` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-parameters.md) for the provider-specific parameters and requirements.

