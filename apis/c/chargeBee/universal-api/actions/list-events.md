# ChargeBee: List Events



```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-events?${params}`, {
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
| `event_type[in]` | list<string> | no | Accepts multiple values in one string. |
| `occurred_at[after]` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_version": "string",
      "content": {},
      "event_type": "string",
      "id": "string",
      "object": "string",
      "occurred_at": 1,
      "source": "string",
      "webhook_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_version` | string |  |
| `content` | object |  |
| `event_type` | string |  |
| `id` | string |  |
| `object` | string |  |
| `occurred_at` | number |  |
| `source` | string |  |
| `webhook_status` | string |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET events` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

