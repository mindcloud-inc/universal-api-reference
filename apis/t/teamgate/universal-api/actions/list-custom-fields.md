# Teamgate: List Custom Fields

Retrieves custom fields from Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-custom-fields?${params}`, {
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
      "id": 1,
      "isActive": "string",
      "isFilter": "string",
      "isList": "string",
      "items": [
        {}
      ],
      "module": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isActive` | string |  |
| `isFilter` | string |  |
| `isList` | string |  |
| `items` | array<object> |  |
| `module` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /customFields` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

