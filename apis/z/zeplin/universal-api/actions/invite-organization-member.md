# Zeplin: Invite Organization Member

Invites a member to a Zeplin organization.

```
POST https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/invite-organization-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/invite-organization-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "handle": "string",
  "tags[]": [
    "string"
  ],
  "role": "string",
  "restricted": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/invite-organization-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "handle": "string",
    "tags[]": ["string"],
    "role": "string",
    "restricted": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Organization id |
| `handle` | string | yes | Email, username or unique identifier of the user |
| `tags[]` | array<string> | yes | Tags of the user in the organization |
| `role` | string | yes | The role of the user in the organization ☝️Note that the Developer role maps to `member` and the Reviewer role maps to `alien` in the API. |
| `restricted` | boolean | yes | Whether the user's membership is restricted to only the projects that they are member of |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invited": 1,
      "restricted": true,
      "role": "string",
      "tags": [
        "string"
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invited` | number |  |
| `restricted` | boolean |  |
| `role` | string |  |
| `tags` | array<string> |  |
| `user` | object |  |

## Native endpoint

Through the native Zeplin API, this operation is `POST /organizations/{organization_id}/members` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-organization-member.md) for the provider-specific parameters and requirements.

