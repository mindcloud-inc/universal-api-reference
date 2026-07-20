# Nautical: List Attributes

Retrieves a list of attributes from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-attributes?${params}`, {
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
        "attributes": {
          "edges": [
            {
              "node": {
                "id": "string",
                "inputType": "string",
                "name": "Ava Chen",
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
| `data.attributes.edges[].node.id` | string |  |
| `data.attributes.edges[].node.inputType` | string |  |
| `data.attributes.edges[].node.name` | string |  |
| `data.attributes.edges[].node.slug` | string |  |
| `data.attributes.pageInfo.endCursor` | string |  |
| `data.attributes.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attributes.md) for the provider-specific parameters and requirements.

