# Typesense: Get Analytics Events

Retrieves recent analytics events from Typesense.

```
GET https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-analytics-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-analytics-events?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/get-analytics-events?${params}`, {
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
| `name` | string | yes | Analytics event name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ],
      "name": "Ava Chen",
      "response": {},
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> |  |
| `name` | string |  |
| `response` | object |  |
| `user_id` | string |  |

## Native endpoint

Through the native Typesense API, this operation is `GET /analytics/events` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-events.md) for the provider-specific parameters and requirements.

