# Mighty Networks: List Space Members

Retrieves members from a space in Mighty Networks.

```
GET https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-space-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-space-members?connectionId=$CONNECTION_ID&limit=25&offset=0&networkId=%7B%7Bcredentials.networkId%7D%7D&spaceId=23049325" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "networkId": "{{credentials.networkId}}",
  "spaceId": "23049325"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/list-space-members?${params}`, {
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
| `spaceId` | number | yes | ID of the space. Example: `23049325`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ambassadorLevel": "string",
      "avatar": "string",
      "bio": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "location": "string",
      "permalink": "https://example.com",
      "referralCount": 1,
      "timeZone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ambassadorLevel` | string |  |
| `avatar` | string |  |
| `bio` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `location` | string |  |
| `permalink` | string |  |
| `referralCount` | number |  |
| `timeZone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `GET /networks/:network_id/spaces/:space_id/members` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-space-members.md) for the provider-specific parameters and requirements.

