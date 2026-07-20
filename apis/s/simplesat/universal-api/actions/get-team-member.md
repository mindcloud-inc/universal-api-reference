# Simplesat: Get Team Member

Retrieves a team member from Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-team-member?connectionId=$CONNECTION_ID&teamMemberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamMemberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-team-member?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamMemberId` | string | yes | The ID of the team member to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_attributes": {},
      "email": "ava@example.com",
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_attributes` | object |  |
| `email` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Simplesat API, this operation is `GET /api/v1/team-members/:team_member_id` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-member.md) for the provider-specific parameters and requirements.

