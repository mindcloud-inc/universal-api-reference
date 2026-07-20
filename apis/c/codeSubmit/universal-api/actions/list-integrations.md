# CodeSubmit: List Integrations



```
GET https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeSubmit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/list-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeSubmit/latest/actions/list-integrations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CodeSubmit API returns.

## Native endpoint

Through the native CodeSubmit API, this operation is `GET /api/company/integrations` (base URL `https://app.codesubmit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.

