# jo4.io: List Team Invitations



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-invitations?connectionId=$CONNECTION_ID&teamSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-invitations?${params}`, {
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
| `teamSlug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedAt": 1,
      "createdTime": 1,
      "email": "ava@example.com",
      "expiresAt": 1,
      "id": 1,
      "invitedBy": 1,
      "invitedByEmail": "ava@example.com",
      "role": "string",
      "slug": "string",
      "status": "string",
      "teamId": 1,
      "teamName": "Ava Chen",
      "teamSlug": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedAt` | number |  |
| `createdTime` | number |  |
| `email` | string |  |
| `expiresAt` | number |  |
| `id` | number |  |
| `invitedBy` | number |  |
| `invitedByEmail` | string |  |
| `role` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `teamId` | number |  |
| `teamName` | string |  |
| `teamSlug` | string |  |
| `token` | string |  |

## Native endpoint

Through the native jo4.io API, this operation is `GET /protected/teams/:teamSlug/invitations` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invitations.md) for the provider-specific parameters and requirements.

