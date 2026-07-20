# Vadootv: Get themes

Retrieves available caption themes from Vadootv.

```
GET https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-themes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-themes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-themes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vadootv API returns.

## Native endpoint

Through the native Vadootv API, this operation is `GET /api/get_themes` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-themes.md) for the provider-specific parameters and requirements.

