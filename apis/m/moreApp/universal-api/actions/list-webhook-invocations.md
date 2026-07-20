# MoreApp: List Webhook Invocations

Retrieves webhook invocations from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-webhook-invocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-webhook-invocations?connectionId=$CONNECTION_ID&customerId=1&subscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "subscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/list-webhook-invocations?${params}`, {
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
| `subscriberId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Invocation records returned for the webhook subscriber. |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}/invocations` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-invocations.md) for the provider-specific parameters and requirements.

