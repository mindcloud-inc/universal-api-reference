# Ubidots: Get all Organizations



```
GET https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubidots `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-organizations?${params}`, {
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
      "app": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dashboardsUrl": "https://example.com",
      "description": "string",
      "devicesUrl": "https://example.com",
      "id": "string",
      "isActive": true,
      "label": "string",
      "logo": "string",
      "name": "Ava Chen",
      "properties": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com",
      "usersUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `createdAt` | date |  |
| `dashboardsUrl` | string |  |
| `description` | string |  |
| `devicesUrl` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `label` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `properties` | object |  |
| `tags` | array<string> |  |
| `url` | string |  |
| `usersUrl` | string |  |

## Native endpoint

Through the native Ubidots API, this operation is `GET /organizations/` (base URL `https://industrial.api.ubidots.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-organizations.md) for the provider-specific parameters and requirements.

