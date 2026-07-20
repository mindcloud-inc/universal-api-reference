# Conveyor: List Access Groups

Retrieves access groups for a program from Conveyor.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-access-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-access-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-access-groups?${params}`, {
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
      "access_groups": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "page": 1,
      "per_page": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_groups` | array<object> |  |
| `access_groups[].id` | string |  |
| `access_groups[].name` | string |  |
| `page` | number |  |
| `per_page` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/exchange/access_groups` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-access-groups.md) for the provider-specific parameters and requirements.

