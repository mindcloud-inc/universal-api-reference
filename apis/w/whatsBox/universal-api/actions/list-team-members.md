# WhatsBox: List Team Members

Retrieves all team members from WhatsBox.

```
GET https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-team-members?${params}`, {
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
      "createdBy": "string",
      "email": "ava@example.com",
      "id": "string",
      "invitedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "role": "string",
      "signedUpAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `email` | string |  |
| `id` | string |  |
| `invitedAt` | date |  |
| `name` | string |  |
| `role` | string |  |
| `signedUpAt` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native WhatsBox API, this operation is `GET /team-members` (base URL `https://api.whatsbox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

