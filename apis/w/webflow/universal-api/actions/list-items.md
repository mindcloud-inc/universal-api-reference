# Webflow: List Items

Retrieves staged collection items from Webflow.

```
GET https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-items?connectionId=$CONNECTION_ID&limit=25&offset=0&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webflow/latest/actions/list-items?${params}`, {
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
| `collectionId` | string | yes | The unique identifier of the collection. |
| `name` | string | no | Optional name selector for returned items. |
| `slug` | string | no | Optional slug selector for returned items. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Number of items to skip before returning results. |
| `limit` | number | no | Maximum number of items to return. |
| `sortBy` | string | no | Field used to sort returned items. |
| `sortOrder` | string | no | Sort direction for returned items. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Collection items returned by the request. |
| `pagination` | object | Pagination metadata for the item list. |

## Native endpoint

Through the native Webflow API, this operation is `GET /collections/:collection_id/items` (base URL `https://api.webflow.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

