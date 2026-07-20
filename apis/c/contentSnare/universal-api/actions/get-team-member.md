# Content Snare: Get Team Member

Retrieves a team member from Content Snare.

```
GET https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-team-member?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-team-member?${params}`, {
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
| `id` | string | yes | Team Member ID. |

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

Through the native Content Snare API, this operation is `GET /partner_api/v1/team_members/{id}` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-member.md) for the provider-specific parameters and requirements.

