# LeadDyno: List Commissions

Retrieves commissions from your LeadDyno account.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-commissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-commissions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/list-commissions?${params}`, {
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
      "commissions": [
        {}
      ],
      "page": 1,
      "per_page": 1,
      "total_entries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commissions` | array<object> |  |
| `page` | number |  |
| `per_page` | number |  |
| `total_entries` | number |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /commissions` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-commissions.md) for the provider-specific parameters and requirements.

