# Facebook: Get Owned Pages



```
GET https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-owned-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Facebook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-owned-pages?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-owned-pages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Facebook API returns.

## Native endpoint

Through the native Facebook API, this operation is `GET :businessId/owned_pages?fields=id,name,access_token` (base URL `https://graph.facebook.com/v23.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-owned-pages.md) for the provider-specific parameters and requirements.

