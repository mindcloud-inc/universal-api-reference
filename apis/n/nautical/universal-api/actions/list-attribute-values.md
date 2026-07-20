# Nautical: List Attribute Values

Retrieves a list of attribute values from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-attribute-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-attribute-values?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-attribute-values?${params}`, {
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
        "attributeValues": {
          "edges": [
            {
              "node": {
                "id": "string",
                "name": "Ava Chen",
                "slug": "string",
                "value": "string"
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
| `data.attributeValues.edges[].node.id` | string |  |
| `data.attributeValues.edges[].node.name` | string |  |
| `data.attributeValues.edges[].node.slug` | string |  |
| `data.attributeValues.edges[].node.value` | string |  |
| `data.attributeValues.pageInfo.endCursor` | string |  |
| `data.attributeValues.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attribute-values.md) for the provider-specific parameters and requirements.

