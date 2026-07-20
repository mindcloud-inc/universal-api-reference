# Nautical: List Export Files

Retrieves a list of export files from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-export-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-export-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-export-files?${params}`, {
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
      "data": {
        "exportFiles": {
          "edges": [
            {
              "node": {
                "createdAt": "string",
                "id": "string",
                "status": "string",
                "updatedAt": "string",
                "url": "https://example.com"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "string",
            "hasNextPage": true
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.exportFiles.edges[].node.createdAt` | string |  |
| `data.exportFiles.edges[].node.id` | string |  |
| `data.exportFiles.edges[].node.status` | string |  |
| `data.exportFiles.edges[].node.updatedAt` | string |  |
| `data.exportFiles.edges[].node.url` | string |  |
| `data.exportFiles.pageInfo.endCursor` | string |  |
| `data.exportFiles.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-export-files.md) for the provider-specific parameters and requirements.

