# Direct Mail Manager: List Postcards



```
GET https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-postcards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-postcards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-postcards?${params}`, {
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
      "cancelled_at": "2026-05-07T12:00:00.000Z",
      "carrier": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "mail_type": "string",
      "name": "Ava Chen",
      "object": "string",
      "size": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled_at` | date |  |
| `carrier` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | string |  |
| `mail_type` | string |  |
| `name` | string |  |
| `object` | string |  |
| `size` | string |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `GET /postcards` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-postcards.md) for the provider-specific parameters and requirements.

