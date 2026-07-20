# ChargeBee: Retrieve Subscription



```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-subscription?connectionId=$CONNECTION_ID&subscription_id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscription_id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/retrieve-subscription?${params}`, {
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
| `subscription_id` | string | yes | The unique identifier of the Chargebee subscription to retrieve. Default: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "currency_code": "string",
      "customer_id": "string",
      "id": "string",
      "mrr": 1,
      "object": "string",
      "status": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `currency_code` | string |  |
| `customer_id` | string |  |
| `id` | string |  |
| `mrr` | number |  |
| `object` | string |  |
| `status` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET subscriptions/:subscription_id` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscription.md) for the provider-specific parameters and requirements.

