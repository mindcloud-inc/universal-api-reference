# Dust: Search Data Source



```
GET https://connect.mindcloud.co/v1/universal/dust/latest/actions/search-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dust/latest/actions/search-data-source?connectionId=$CONNECTION_ID&dataSourceId=string&query=string&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "string",
  "query": "string",
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dust/latest/actions/search-data-source?${params}`, {
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
| `dataSourceId` | string | yes | Dust data source sId. |
| `query` | string | yes | Search query string. |
| `spaceId` | string | yes | Dust space sId. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dust API returns.

## Native endpoint

Through the native Dust API, this operation is `POST /api/v1/w/:workspaceId/spaces/:spaceId/data_sources/:dataSourceId/search` (base URL `https://dust.tt`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-data-source.md) for the provider-specific parameters and requirements.

