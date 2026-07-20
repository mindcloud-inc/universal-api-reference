# AI/ML API: Get Account Balance

Retrieves the account balance from AI/ML API.

```
GET https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/get-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI/ML API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/get-account-balance?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AI/ML API API returns.

## Native endpoint

Through the native AI/ML API API, this operation is `GET /v1/billing/balance` (base URL `https://api.aimlapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-balance.md) for the provider-specific parameters and requirements.

