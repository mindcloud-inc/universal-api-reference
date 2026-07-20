# HappyDesk: Get Knowledge Sections



```
GET https://connect.mindcloud.co/v1/universal/happyDesk/latest/actions/get-knowledge-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyDesk/latest/actions/get-knowledge-sections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyDesk/latest/actions/get-knowledge-sections?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HappyDesk API returns.

## Native endpoint

Through the native HappyDesk API, this operation is `GET /knowledge/section` (base URL `{{credentials.tenantUrl}}/panel/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-sections.md) for the provider-specific parameters and requirements.

