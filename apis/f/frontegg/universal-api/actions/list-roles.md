# Frontegg: List Roles

Finds roles in your Frontegg environment.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/list-roles?${params}`, {
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
      "createdAt": "string",
      "description": "string",
      "firstUserRole": true,
      "id": "string",
      "isDefault": true,
      "key": "string",
      "level": 1,
      "name": "Ava Chen",
      "tenantId": {},
      "updatedAt": "string",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `firstUserRole` | boolean |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `key` | string |  |
| `level` | number |  |
| `name` | string |  |
| `tenantId` | object |  |
| `updatedAt` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /identity/resources/roles/v1` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-roles.md) for the provider-specific parameters and requirements.

