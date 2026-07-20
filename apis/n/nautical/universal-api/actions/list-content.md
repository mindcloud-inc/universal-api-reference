# Nautical: List Content

Retrieves a list of content from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-content?${params}`, {
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
        "contentList": {
          "edges": [
            {
              "node": {
                "id": "string",
                "isPublished": true,
                "publicationDate": "string",
                "slug": "string"
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
| `data.contentList.edges[].node.id` | string |  |
| `data.contentList.edges[].node.isPublished` | boolean |  |
| `data.contentList.edges[].node.publicationDate` | string |  |
| `data.contentList.edges[].node.slug` | string |  |
| `data.contentList.pageInfo.endCursor` | string |  |
| `data.contentList.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content.md) for the provider-specific parameters and requirements.

