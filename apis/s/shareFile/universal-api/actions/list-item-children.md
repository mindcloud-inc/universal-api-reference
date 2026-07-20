# ShareFile: List Item Children



```
GET https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/list-item-children
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/list-item-children?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/list-item-children?${params}`, {
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
| `id` | string | yes | The ShareFile item identifier whose children should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "odata": {
        "count": 1,
        "metadata": "string"
      },
      "url": "https://example.com",
      "value": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `odata.count` | number | The total child-item count returned by ShareFile. |
| `odata.metadata` | string | The OData metadata URL for the child-items collection. |
| `url` | string | The API URL for the child-items collection. |
| `value` | array<object> | The list of child items under the requested parent item. |

## Native endpoint

Through the native ShareFile API, this operation is `GET /Items({{id}})/Children` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-item-children.md) for the provider-specific parameters and requirements.

