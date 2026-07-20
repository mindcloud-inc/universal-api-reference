# Nautical: List Import Files

Retrieves a list of import files from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-import-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-import-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-import-files?${params}`, {
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
        "importFiles": {
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
| `data.importFiles.edges[].node.createdAt` | string |  |
| `data.importFiles.edges[].node.id` | string |  |
| `data.importFiles.edges[].node.status` | string |  |
| `data.importFiles.edges[].node.updatedAt` | string |  |
| `data.importFiles.edges[].node.url` | string |  |
| `data.importFiles.pageInfo.endCursor` | string |  |
| `data.importFiles.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-import-files.md) for the provider-specific parameters and requirements.

