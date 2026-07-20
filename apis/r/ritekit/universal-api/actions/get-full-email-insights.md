# Ritekit: Get Full Email Insights

Retrieves full email insights from Ritekit.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-full-email-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-full-email-insights?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-full-email-insights?${params}`, {
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
| `email` | string | yes | Email address to analyze for person insights. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disposable": true,
      "domain": "string",
      "freemail": true,
      "message": "string",
      "name": "Ava Chen",
      "result": true,
      "suggestions": [
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
| `disposable` | boolean |  |
| `domain` | string |  |
| `freemail` | boolean |  |
| `message` | string |  |
| `name` | string |  |
| `result` | boolean |  |
| `suggestions` | array<string> |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/person-insights/full-email-insights` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-email-insights.md) for the provider-specific parameters and requirements.

