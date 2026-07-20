# MoreApp: List Webhook Events

Retrieves webhook events from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-webhook-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-webhook-events?connectionId=$CONNECTION_ID&customerId=209321" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-webhook-events?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `page` | string | no | Optional event page number. |
| `size` | string | no | Optional page size. |
| `type` | string | no | Optional webhook event type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": 1,
      "data": {},
      "id": "string",
      "timestamp": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | number |  |
| `data` | object |  |
| `id` | string |  |
| `timestamp` | string |  |
| `type` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/webhooks/customer/{{customerId}}/events` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-events.md) for the provider-specific parameters and requirements.

