# Qlik: List Item Collections

Retrieves the collections for an item in Qlik.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-item-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-item-collections?connectionId=$CONNECTION_ID&limit=25&offset=0&itemId=65b8f2a1f4b0c2d3e4f56789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "itemId": "65b8f2a1f4b0c2d3e4f56789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/list-item-collections?${params}`, {
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
| `itemId` | string | yes | Qlik item ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
          "itemCount": 1,
          "name": "Ava Chen",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].id` | string |  |
| `data[].itemCount` | number |  |
| `data[].name` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/items/:itemId/collections` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-item-collections.md) for the provider-specific parameters and requirements.

