# Content Snare: Update Team Member

Updates a team member in Content Snare.

```
PUT https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/update-team-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Team Member ID. |
| `active` | boolean | no | Active (true) or inactive (false). It's false if user is not allowed to use the system. |
| `role` | string | no | The user’s current role |

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

Through the native Content Snare API, this operation is `PUT /partner_api/v1/team_members/{id}` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-member.md) for the provider-specific parameters and requirements.

