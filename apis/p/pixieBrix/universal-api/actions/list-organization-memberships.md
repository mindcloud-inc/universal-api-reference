# PixieBrix: List Organization Memberships

Retrieves memberships for an organization in PixieBrix.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-organization-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-organization-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationPk=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationPk": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-organization-memberships?${params}`, {
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
| `organizationPk` | string | yes | PixieBrix organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groups": [
        {}
      ],
      "id": 1,
      "last_active_at": "2026-05-07T12:00:00.000Z",
      "last_login_at": "2026-05-07T12:00:00.000Z",
      "role": 1,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groups` | array<object> |  |
| `id` | number |  |
| `last_active_at` | date |  |
| `last_login_at` | date |  |
| `role` | number |  |
| `user` | object |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/organizations/:organization_pk/memberships/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organization-memberships.md) for the provider-specific parameters and requirements.

