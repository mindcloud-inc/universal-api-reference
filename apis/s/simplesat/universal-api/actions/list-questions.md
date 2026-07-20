# Simplesat: List Questions

Retrieves questions from Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-questions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-questions?${params}`, {
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
| `pageSize` | number | no | The number of questions to return per page |
| `page` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | no | Filter questions by survey ID |
| `metric` | string | no | Filter questions by metric |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        "string"
      ],
      "id": 1,
      "metric": "string",
      "order": 1,
      "rating_scale": true,
      "required": true,
      "rules": [
        {}
      ],
      "survey": {},
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<string> |  |
| `id` | number |  |
| `metric` | string |  |
| `order` | number |  |
| `rating_scale` | boolean |  |
| `required` | boolean |  |
| `rules` | array<object> |  |
| `survey` | object |  |
| `text` | string |  |

## Native endpoint

Through the native Simplesat API, this operation is `GET /api/v1/questions` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

