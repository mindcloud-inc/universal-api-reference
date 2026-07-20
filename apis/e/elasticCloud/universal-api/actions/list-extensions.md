# Elastic Cloud: List Extensions

Retrieves extensions from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-extensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-extensions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-extensions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Elastic Cloud API returns.

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/extensions` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-extensions.md) for the provider-specific parameters and requirements.

