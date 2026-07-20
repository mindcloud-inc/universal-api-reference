# Customer.io: List Subscription Topics

Retrieves subscription topics from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-subscription-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-subscription-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-subscription-topics?${params}`, {
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
      "description": "string",
      "id": 1,
      "identifier": "string",
      "name": "Ava Chen",
      "subscribedByDefault": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | The description of the subscription topic. |
| `id` | number | The system-generated id for the subscription topic. |
| `identifier` | string | The key associated with the subscription topic. |
| `name` | string | The name of the subscription topic. |
| `subscribedByDefault` | boolean | Whether people are subscribed to the topic by default. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/subscription_topics` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscription-topics.md) for the provider-specific parameters and requirements.

