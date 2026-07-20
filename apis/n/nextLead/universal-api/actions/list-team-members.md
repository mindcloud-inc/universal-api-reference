# NextLead: List Team Members

Retrieves your organization's team members from NextLead.

```
GET https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/list-team-members?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailVerified": true,
      "firstName": "Ava",
      "id": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "organizationOwner": true,
      "phone": "string",
      "role": "string",
      "twoFactorEnabled": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `firstName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `organizationOwner` | boolean |  |
| `phone` | string |  |
| `role` | string |  |
| `twoFactorEnabled` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native NextLead API, this operation is `GET /api/v2/receive/contact/get-team` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

