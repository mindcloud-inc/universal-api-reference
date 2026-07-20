# Heyy: Get Business

Retrieves business details for a Heyy workspace.

```
GET https://connect.mindcloud.co/v1/universal/heyy/latest/actions/get-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/get-business?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/get-business?${params}`, {
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
      "authTenantId": "string",
      "availability": [
        {}
      ],
      "branding": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authTenantId` | string |  |
| `availability` | array<object> |  |
| `branding` | object |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `timezone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Heyy API, this operation is `GET /business` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business.md) for the provider-specific parameters and requirements.

