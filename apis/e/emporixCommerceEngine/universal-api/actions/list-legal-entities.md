# Emporix Commerce Engine: List Legal Entities

Retrieves legal entities from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-legal-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-legal-entities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-legal-entities?${params}`, {
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
      "accountLimit": {},
      "customerGroups": [
        {}
      ],
      "entitiesAddresses": [
        {}
      ],
      "id": "string",
      "legalInfo": {},
      "metadata": {},
      "name": "Ava Chen",
      "parentId": "string",
      "restrictions": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountLimit` | object |  |
| `customerGroups` | array<object> |  |
| `entitiesAddresses` | array<object> |  |
| `id` | string |  |
| `legalInfo` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `parentId` | string |  |
| `restrictions` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /customer-management/{{credentials.tenantId}}/legal-entities` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-legal-entities.md) for the provider-specific parameters and requirements.

