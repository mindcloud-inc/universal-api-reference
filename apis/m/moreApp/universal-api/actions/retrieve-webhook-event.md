# MoreApp: Retrieve Webhook Event

Retrieves a webhook event from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-webhook-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-webhook-event?connectionId=$CONNECTION_ID&customerId=1&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/retrieve-webhook-event?${params}`, {
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
| `customerId` | number | yes |  |
| `eventId` | string | yes |  |

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

Through the native MoreApp API, this operation is `GET /api/v1.0/webhooks/customer/{{customerId}}/events/{{eventId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook-event.md) for the provider-specific parameters and requirements.

