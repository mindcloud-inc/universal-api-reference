# Sympla: List Events

Retrieves the organizer's events from Sympla.

```
GET https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sympla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-events?${params}`, {
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
| `from` | string | no | Filter events that start on or after this datetime in YYYY-MM-DD HH:mm:ss format. |
| `published` | boolean | no | When true, only published events are returned. |
| `fields` | string | no | Optional comma-separated response fields to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pagination": {},
      "sort": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `pagination` | object |  |
| `sort` | object |  |

## Native endpoint

Through the native Sympla API, this operation is `GET /events` (base URL `https://api.sympla.com.br/public/v1.5.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

