# Frontegg: List Permissions

Finds permissions in your Frontegg environment.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-permissions?${params}`, {
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
      "assignmentType": "string",
      "categoryId": "string",
      "createdAt": "string",
      "description": "string",
      "fePermission": true,
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "roleIds": [
        "string"
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignmentType` | string |  |
| `categoryId` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `fePermission` | boolean |  |
| `id` | string |  |
| `key` | string |  |
| `name` | string |  |
| `roleIds[]` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /identity/resources/permissions/v1` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-permissions.md) for the provider-specific parameters and requirements.

