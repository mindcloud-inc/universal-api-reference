# Avoma: Get Meeting Insights

Retrieves insights for a completed meeting from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-insights?connectionId=$CONNECTION_ID&meetingUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-insights?${params}`, {
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
| `meetingUuid` | string | yes | Unique ID of the meeting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiNotes": [
        {
          "end": 1,
          "noteType": "string",
          "speakerId": 1,
          "start": 1,
          "text": "string",
          "uuid": "string"
        }
      ],
      "keywords": {
        "occurrences": [
          {
            "category": "string",
            "count": 1,
            "isRep": true,
            "keywords": [
              {
                "count": 1,
                "word": "string"
              }
            ],
            "speakerId": 1
          }
        ],
        "popular": [
          {
            "count": 1,
            "score": 1,
            "word": "string"
          }
        ]
      },
      "speakers": [
        {
          "email": "ava@example.com",
          "id": 1,
          "isRep": true,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiNotes[].end` | number |  |
| `aiNotes[].noteType` | string |  |
| `aiNotes[].speakerId` | number |  |
| `aiNotes[].start` | number |  |
| `aiNotes[].text` | string |  |
| `aiNotes[].uuid` | string |  |
| `keywords.occurrences[].category` | string |  |
| `keywords.occurrences[].count` | number |  |
| `keywords.occurrences[].isRep` | boolean |  |
| `keywords.occurrences[].keywords[].count` | number |  |
| `keywords.occurrences[].keywords[].word` | string |  |
| `keywords.occurrences[].speakerId` | number |  |
| `keywords.popular[].count` | number |  |
| `keywords.popular[].score` | number |  |
| `keywords.popular[].word` | string |  |
| `speakers[].email` | string |  |
| `speakers[].id` | number |  |
| `speakers[].isRep` | boolean |  |
| `speakers[].name` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/meetings/:meetingUuid/insights/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-insights.md) for the provider-specific parameters and requirements.

