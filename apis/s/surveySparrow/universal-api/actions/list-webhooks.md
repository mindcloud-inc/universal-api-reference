# SurveySparrow: List Webhooks

Retrieves all webhooks from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-webhooks?${params}`, {
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
| `surveyId` | number | no | ID of the survey |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "disabled": true,
      "event_type": "string",
      "headers": [
        {}
      ],
      "http_method": "string",
      "id": 1,
      "name": "Ava Chen",
      "object_type": "string",
      "properties": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `disabled` | boolean |  |
| `event_type` | string |  |
| `headers` | array<object> |  |
| `http_method` | string |  |
| `id` | number |  |
| `name` | string |  |
| `object_type` | string |  |
| `properties` | object |  |
| `url` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /webhooks` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

