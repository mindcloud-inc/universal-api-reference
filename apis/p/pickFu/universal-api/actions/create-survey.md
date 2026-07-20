# PickFu: Create Survey



```
POST https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `questions[]` | array<object> | yes | List of questions for the survey. |
| `targeting[]` | array<string> | no | Demographic targeting traits. |
| `reporting[]` | array<string> | no | Reporting breakdown traits. |
| `country` | string | no | Two-letter country code. |
| `sampleSize` | string | no | Number of respondents. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyIntent` | string | no | Original intent of the survey as interpreted by AI. |
| `isMiniPoll` | boolean | no | Whether to create this survey as a daily mini-poll. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "id": "string",
      "name": "Ava Chen",
      "numResponses": 1,
      "questions": [
        {}
      ],
      "reporting": [
        "string"
      ],
      "sampleSize": 1,
      "status": "string",
      "surveyUrl": "https://example.com",
      "targeting": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `id` | string |  |
| `name` | string |  |
| `numResponses` | number |  |
| `questions` | array<object> |  |
| `reporting` | array<string> |  |
| `sampleSize` | number |  |
| `status` | string |  |
| `surveyUrl` | string |  |
| `targeting` | array<string> |  |

## Native endpoint

Through the native PickFu API, this operation is `POST /surveys` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey.md) for the provider-specific parameters and requirements.

