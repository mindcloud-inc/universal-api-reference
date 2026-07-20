# Workiz: Get Team Member

Retrieves a team member from Workiz by user ID.

```
GET https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-team-member?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-team-member?${params}`, {
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
| `userId` | string | yes | The user's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": "string",
      "email": "ava@example.com",
      "fieldTech": true,
      "id": "string",
      "name": "Ava Chen",
      "role": "string",
      "serviceAreas": [
        "string"
      ],
      "skills": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | string |  |
| `email` | string |  |
| `fieldTech` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `role` | string |  |
| `serviceAreas` | array<string> |  |
| `skills` | array<string> |  |

## Native endpoint

Through the native Workiz API, this operation is `GET /team/get/:USER_ID/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-member.md) for the provider-specific parameters and requirements.

