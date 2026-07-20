# Mighty Networks: Get Current User

Retrieves the current user from Mighty Networks.

```
GET https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-current-user?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `networkId` | string | yes | The Mighty Networks network ID or subdomain for the request path. Default: `{{credentials.networkId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "network": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": 1,
        "purpose": "string",
        "subdomain": "string",
        "subtitle": "string",
        "title": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "user": {
        "admin": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "shortBio": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `network` | object |  |
| `network.createdAt` | date |  |
| `network.description` | string |  |
| `network.id` | number |  |
| `network.purpose` | string |  |
| `network.subdomain` | string |  |
| `network.subtitle` | string |  |
| `network.title` | string |  |
| `network.updatedAt` | date |  |
| `user` | object |  |
| `user.admin` | boolean |  |
| `user.createdAt` | date |  |
| `user.email` | string |  |
| `user.id` | number |  |
| `user.name` | string |  |
| `user.shortBio` | string |  |
| `user.updatedAt` | date |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `GET /networks/:network_id/me` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

