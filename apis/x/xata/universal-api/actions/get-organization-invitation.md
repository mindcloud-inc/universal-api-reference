# Xata: Get details of a specific invitation



```
GET https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organization-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organization-invitation?connectionId=$CONNECTION_ID&organizationID=string&invitationID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationID": "string",
  "invitationID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organization-invitation?${params}`, {
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
| `organizationID` | string | yes | Unique identifier for a specific organization |
| `invitationID` | string | yes | Unique identifier for an invitation |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "first_name": "Ava",
      "id": "string",
      "invite_link": "https://example.com",
      "last_name": "Chen",
      "organization_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Timestamp when the invitation was created |
| `email` | string | Email address of the invited user |
| `expires_at` | date | Timestamp when the invitation expires |
| `first_name` | string | First name of the invited user |
| `id` | string | Unique identifier for the invitation |
| `invite_link` | string | URL link to accept the invitation |
| `last_name` | string | Last name of the invited user |
| `organization_id` | string | ID of the organization the invitation is for |
| `status` | string | Current status of the invitation |

## Native endpoint

Through the native Xata API, this operation is `GET /organizations/:organizationID/invitations/:invitationID` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-invitation.md) for the provider-specific parameters and requirements.

