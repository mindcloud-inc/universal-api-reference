# Weaviate Vector Store: Add Collection Property

Adds a property to a collection in Weaviate.

```
PUT https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/add-collection-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/add-collection-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "className": "Ava Chen",
  "dataType[0]": "text",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/add-collection-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "className": "Ava Chen",
    "dataType[0]": "text",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `className` | string | yes | The collection class name to update. |
| `dataType[0]` | string | yes | The property data type to add. Default: `text`. |
| `name` | string | yes | The property name to add. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataType": [
        [
          "string"
        ]
      ],
      "indexFilterable": true,
      "indexRangeFilters": true,
      "indexSearchable": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataType[]` | array<string> |  |
| `indexFilterable` | boolean |  |
| `indexRangeFilters` | boolean |  |
| `indexSearchable` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `POST /v1/schema/:className/properties` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-collection-property.md) for the provider-specific parameters and requirements.

