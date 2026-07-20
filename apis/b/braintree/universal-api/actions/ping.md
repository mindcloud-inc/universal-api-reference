# Braintree: Ping

Retrieves a ping response from Braintree.

```
GET https://connect.mindcloud.co/v1/universal/braintree/latest/actions/ping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Braintree `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/braintree/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/braintree/latest/actions/ping?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Braintree API returns.

## Native endpoint

Through the native Braintree API, this operation is `POST /graphql` (base URL `https://payments.sandbox.braintree-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping.md) for the provider-specific parameters and requirements.

