# fal.ai: List Billing Events

Retrieves billing event records from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-billing-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-billing-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/list-billing-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_events": [
        {}
      ],
      "has_more": true,
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_events` | array<object> |  |
| `has_more` | boolean |  |
| `next_cursor` | string |  |

## Native endpoint

Through the native fal.ai API, this operation is `GET /models/billing-events` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-events.md) for the provider-specific parameters and requirements.

