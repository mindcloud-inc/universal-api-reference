# Webling: List Documentgroups



```
GET https://connect.mindcloud.co/v1/universal/webling/latest/actions/list-documentgroups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webling/latest/actions/list-documentgroups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webling/latest/actions/list-documentgroups?${params}`, {
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
| `filter` | string | no | Filter the document group list using Webling query language. |
| `order` | string | no | Sort the document group list by property and direction. |
| `format` | string | no | Optional Webling response format. Default: `full`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": {},
      "id": 1,
      "links": {},
      "meta": {},
      "parents": [
        1
      ],
      "properties": {},
      "readonly": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | object |  |
| `id` | number |  |
| `links` | object |  |
| `meta` | object |  |
| `parents` | array<number> |  |
| `properties` | object |  |
| `readonly` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Webling API, this operation is `GET /documentgroup` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documentgroups.md) for the provider-specific parameters and requirements.

