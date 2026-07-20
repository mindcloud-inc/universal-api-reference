# Pipio: List Languages

Finds supported voice languages in Pipio.

```
GET https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipio/latest/actions/list-languages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pipio API returns.

## Native endpoint

Through the native Pipio API, this operation is `GET /actor/languages/all` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-languages.md) for the provider-specific parameters and requirements.

