# Enrich.so: List Pending Invitations

Retrieves pending team invitations from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-pending-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-pending-invitations?connectionId=$CONNECTION_ID&teamId=team_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "team_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-pending-invitations?${params}`, {
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
| `teamId` | string | yes | Enrich team ID. Default: `team_example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Invitation creation timestamp. |
| `email` | string | Invitee email address. |
| `expiresAt` | date | Invitation expiration timestamp. |
| `id` | string | Invitation identifier. |
| `role` | string | Role assigned by the invitation. |
| `status` | string | Invitation status. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /teams/{teamId}/invitations` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-invitations.md) for the provider-specific parameters and requirements.

