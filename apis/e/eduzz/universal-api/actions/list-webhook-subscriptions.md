# Eduzz: List Webhook Subscriptions

Retrieves all webhook subscriptions from Eduzz.

```
GET https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/list-webhook-subscriptions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `GET /webhook/v1/subscription` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

