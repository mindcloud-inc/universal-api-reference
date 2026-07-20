# UserBit: Create Survey Response

Creates a survey response in UserBit.

```
POST https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-survey-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserBit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-survey-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userBit/latest/actions/create-survey-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "questionId": "string",
      "surveyId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Response creation timestamp. |
| `id` | string | Survey response identifier. |
| `questionId` | string | Survey question identifier. |
| `surveyId` | string | Survey identifier. |

## Native endpoint

Through the native UserBit API, this operation is `POST /v1/surveys/questions/list` (base URL `https://userbit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey-response.md) for the provider-specific parameters and requirements.

