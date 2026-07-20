# Freshsales Classic: List Contact Views

Retrieves contact views from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-views?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-contact-views?${params}`, {
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
      "currentUserPermissions": [
        "string"
      ],
      "id": 1,
      "isDefault": true,
      "modelClassName": "Ava Chen",
      "name": "Ava Chen",
      "updatedAt": "string",
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentUserPermissions` | array<string> |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `modelClassName` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |
| `userName` | string |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /contacts/filters` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-views.md) for the provider-specific parameters and requirements.

