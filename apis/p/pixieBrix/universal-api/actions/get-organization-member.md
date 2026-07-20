# PixieBrix: Get Organization Member

Retrieves an organization member from PixieBrix.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-organization-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-organization-member?connectionId=$CONNECTION_ID&id=string&organizationPk=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "organizationPk": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-organization-member?${params}`, {
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
| `id` | string | yes | PixieBrix user UUID for the organization member. |
| `organizationPk` | string | yes | PixieBrix organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_joined": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "groups": [
        {}
      ],
      "id": "string",
      "last_login": "2026-05-07T12:00:00.000Z",
      "last_used_mod_at": "2026-05-07T12:00:00.000Z",
      "membership": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_joined` | date |  |
| `email` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `last_login` | date |  |
| `last_used_mod_at` | date |  |
| `membership` | object |  |
| `name` | string |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/organizations/:organization_pk/members/:id/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-member.md) for the provider-specific parameters and requirements.

