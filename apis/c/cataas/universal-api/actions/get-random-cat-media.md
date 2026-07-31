# Cataas: Get Random Cat Media



```
GET https://connect.mindcloud.co/v1/universal/cataas/latest/actions/get-random-cat-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cataas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cataas/latest/actions/get-random-cat-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cataas/latest/actions/get-random-cat-media?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cataas API returns.

## Native endpoint

Through the native Cataas API, this operation is `GET /cat` (base URL `https://cataas.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-cat-media.md) for the provider-specific parameters and requirements.

