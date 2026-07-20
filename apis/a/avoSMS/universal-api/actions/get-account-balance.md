# AvoSMS: Get Account Balance

Retrieves your account balance from AvoSMS.

```
GET https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-account-balance?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/account/balance` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-balance.md) for the provider-specific parameters and requirements.

