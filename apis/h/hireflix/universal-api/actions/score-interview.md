# Hireflix: Score Interview

Updates an interview score in Hireflix.

```
PUT https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/score-interview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/score-interview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string",
  "variables.score": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/score-interview', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string",
    "variables.score": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.id` | string | yes | The Hireflix interview ID. |
| `variables.score` | number | yes | The score to assign to the interview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "score": {
        "type": "string",
        "value": 1
      },
      "scores": [
        {
          "computedScore": 1,
          "id": "string",
          "overridenScore": {
            "value": 1
          }
        }
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `score.type` | string |  |
| `score.value` | number |  |
| `scores[].computedScore` | number |  |
| `scores[].id` | string |  |
| `scores[].overridenScore.value` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/score-interview.md) for the provider-specific parameters and requirements.

