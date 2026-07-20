# Nautical: List Media

Retrieves a list of media from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-media?${params}`, {
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
        "mediaList": {
          "edges": [
            {
              "node": {
                "alt": "string",
                "createdAt": "string",
                "id": "string",
                "title": "string"
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
| `data.mediaList.edges[].node.alt` | string |  |
| `data.mediaList.edges[].node.createdAt` | string |  |
| `data.mediaList.edges[].node.id` | string |  |
| `data.mediaList.edges[].node.title` | string |  |
| `data.mediaList.pageInfo.endCursor` | string |  |
| `data.mediaList.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

