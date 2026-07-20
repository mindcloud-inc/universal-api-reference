# ClickHouse: Get Invitation



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-invitation?connectionId=$CONNECTION_ID&organizationId=string&invitationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "invitationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-invitation?${params}`, {
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
| `organizationId` | string | yes | ID of the requested organization. |
| `invitationId` | string | yes | ID of the requested invitation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedRoles": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expireAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedRoles` | array<object> | Roles assigned when the invitation is accepted. |
| `createdAt` | date | Invitation creation timestamp. |
| `email` | string | Email of the invited user. |
| `expireAt` | date | Invitation expiration timestamp. |
| `id` | string | Unique invitation ID. |
| `role` | string | Deprecated invited user role. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/invitations/[:invitationId]` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invitation.md) for the provider-specific parameters and requirements.

