# Zammad: List Organizations

Retrieves organizations from Zammad.

```
GET https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-organizations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zammad API returns.

## Native endpoint

Through the native Zammad API, this operation is `GET /organizations` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

