# Apiary: List APIs

Finds APIs in your Apiary account.

```
GET https://connect.mindcloud.co/v1/universal/apiary/latest/actions/list-ap-is
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apiary/latest/actions/list-ap-is?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apiary/latest/actions/list-ap-is?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apiary API returns.

## Native endpoint

Through the native Apiary API, this operation is `GET /me/apis` (base URL `https://api.apiary.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ap-is.md) for the provider-specific parameters and requirements.

