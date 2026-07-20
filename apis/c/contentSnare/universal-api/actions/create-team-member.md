# Content Snare: Create Team Member

Creates a team member in Content Snare.

```
POST https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "fullName": "Ava Chen",
  "role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/create-team-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "fullName": "Ava Chen",
    "role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email address |
| `fullName` | string | yes | Contact full name |
| `personalMessage` | string | no | The message is included in the invitation email |
| `phone` | string | no | Phone number |
| `role` | string | yes | The user’s current role |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatar": "string",
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": "string",
      "phone": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatar` | string |  |
| `company_name` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `phone` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `POST /partner_api/v1/team_members` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team-member.md) for the provider-specific parameters and requirements.

