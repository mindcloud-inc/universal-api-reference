# Billforward: List Payment Methods

Retrieves payment methods from Billforward.

```
GET https://connect.mindcloud.co/v1/universal/billforward/latest/actions/list-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billforward `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billforward/latest/actions/list-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billforward/latest/actions/list-payment-methods?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billforward API returns.

## Native endpoint

Through the native Billforward API, this operation is `GET /payment-methods` (base URL `https://app-sandbox.billforward.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-methods.md) for the provider-specific parameters and requirements.

