# ChargeBee: Retrieve Event

Retrieves an event from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-event?connectionId=$CONNECTION_ID&event_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-event?${params}`, {
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
| `event_id` | string | yes | The Chargebee event identifier. |

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

Through the native ChargeBee API, this operation is `GET events/:event_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-event.md) for the provider-specific parameters and requirements.

