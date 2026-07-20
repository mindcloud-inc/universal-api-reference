# Recreation.gov: List Public Assets



```
GET https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-public-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-public-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-public-assets?${params}`, {
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
| `assetTypes[]` | array<string> | no | Accepts multiple values as an array. |
| `orgIds[]` | array<number> | no | Accepts multiple values as an array. |
| `activity` | string | no |  |
| `state` | string | no |  |
| `terms` | string | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |
| `sort` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "org_id": "string",
      "org_name": "Ava Chen",
      "reservable": true,
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `org_id` | string |  |
| `org_name` | string |  |
| `reservable` | boolean |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `GET /public/assets` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-public-assets.md) for the provider-specific parameters and requirements.

