# Grafana: Search Resources

Finds folders and dashboards in Grafana by query.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/search-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/search-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/search-resources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "folderTitle": "string",
      "folderUid": "string",
      "id": 1,
      "isDeleted": true,
      "isStarred": true,
      "orgId": 1,
      "title": "string",
      "type": "string",
      "uid": "string",
      "uri": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderTitle` | string |  |
| `folderUid` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `isStarred` | boolean |  |
| `orgId` | number |  |
| `title` | string |  |
| `type` | string |  |
| `uid` | string |  |
| `uri` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /search` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-resources.md) for the provider-specific parameters and requirements.

