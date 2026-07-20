# Direct Mail Manager: Get Segment



```
GET https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/get-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/get-segment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/get-segment?${params}`, {
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
      "conditions": [
        {}
      ],
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "total": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditions` | array<object> |  |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `total` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `GET /segments/:sgm_id` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segment.md) for the provider-specific parameters and requirements.

