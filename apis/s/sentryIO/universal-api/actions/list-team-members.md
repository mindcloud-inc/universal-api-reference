# Sentry IO: List Team Members

Retrieves members from a Sentry IO team.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-team-members?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&teamIdOrSlug=my-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "teamIdOrSlug": "my-team"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-team-members?${params}`, {
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
| `organizationIdOrSlug` | string | yes | The Sentry organization ID or slug. Example: `my-org`. |
| `teamIdOrSlug` | string | yes | The Sentry team ID or slug. Example: `my-team`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "role": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Member email address. |
| `id` | string | Member identifier. |
| `name` | string | Member display name. |
| `role` | string | Member role. |
| `user` | object | Linked user object. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /teams/:organization_id_or_slug/:team_id_or_slug/members/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

