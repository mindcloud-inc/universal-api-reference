# CallerAPI: List Webhook Subscriptions

Retrieves webhook subscriptions from CallerAPI.

```
GET https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallerAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/list-webhook-subscriptions?${params}`, {
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
      "data": [
        {
          "active": true,
          "created_at": "string",
          "id": "string",
          "url": "https://example.com"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Webhook subscriptions for the current account. CallerAPI returned null for an empty set in runtime testing; docs show this field as an array when subscriptions exist. |
| `data[].active` | boolean | Whether the subscription is active. |
| `data[].created_at` | string | Timestamp when the subscription was created. |
| `data[].id` | string | Webhook subscription identifier. |
| `data[].url` | string | Webhook destination URL. |
| `status` | string | CallerAPI response status. |

## Native endpoint

Through the native CallerAPI API, this operation is `GET /api/webhooks/complaints/subscriptions` (base URL `https://api.callerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

