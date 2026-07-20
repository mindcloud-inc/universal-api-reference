# Superglue: List End Users



```
GET https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-end-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-end-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-end-users?${params}`, {
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
      "allowedSystems": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedSystems` | array<string> | System IDs this user can access. |
| `createdAt` | date | End user creation timestamp. |
| `email` | string | End user email address. |
| `externalId` | string | Application-defined external user ID. |
| `id` | string | Internal Superglue end user ID. |
| `metadata` | object | Custom metadata for the end user. |
| `name` | string | End user display name. |
| `updatedAt` | date | End user update timestamp. |

## Native endpoint

Through the native Superglue API, this operation is `GET /end-users` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-end-users.md) for the provider-specific parameters and requirements.

