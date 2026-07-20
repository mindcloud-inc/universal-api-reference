# Straker Verify: Get Token Balance

Retrieves your token balance from Straker Verify.

```
GET https://connect.mindcloud.co/v1/universal/strakerVerify/latest/actions/get-token-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Straker Verify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strakerVerify/latest/actions/get-token-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strakerVerify/latest/actions/get-token-balance?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Straker Verify API returns.

## Native endpoint

Through the native Straker Verify API, this operation is `GET /user/balance` (base URL `https://api-verify.straker.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-balance.md) for the provider-specific parameters and requirements.

