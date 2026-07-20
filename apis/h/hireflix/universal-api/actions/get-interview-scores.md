# Hireflix: Get Interview Scores

Retrieves scoring details for an interview in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview-scores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview-scores?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview-scores?${params}`, {
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
| `variables.id` | string | yes | The Hireflix interview ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "score": {
        "type": "string",
        "value": 1
      },
      "scores": [
        {
          "computedScore": 1,
          "id": "string",
          "overridenScore": {
            "createdAt": 1,
            "updatedAt": 1,
            "value": 1
          },
          "scorer": {
            "__typename": "Ava Chen",
            "deleted": true,
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          }
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
| `score.type` | string |  |
| `score.value` | number |  |
| `scores[].computedScore` | number |  |
| `scores[].id` | string |  |
| `scores[].overridenScore.createdAt` | number |  |
| `scores[].overridenScore.updatedAt` | number |  |
| `scores[].overridenScore.value` | number |  |
| `scores[].scorer.__typename` | string |  |
| `scores[].scorer.deleted` | boolean |  |
| `scores[].scorer.email` | string |  |
| `scores[].scorer.id` | string |  |
| `scores[].scorer.name` | string |  |
| `scores[].scorer.type` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interview-scores.md) for the provider-specific parameters and requirements.

