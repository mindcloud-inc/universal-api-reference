# Sentry IO: List Project Users

Retrieves users from a Sentry IO project.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-project-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-project-users?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&projectIdOrSlug=my-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "projectIdOrSlug": "my-project"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-project-users?${params}`, {
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
| `projectIdOrSlug` | string | yes | The Sentry project ID or slug. Example: `my-project`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "hash": "string",
      "id": "string",
      "identifier": "string",
      "ipAddress": "string",
      "name": "Ava Chen",
      "tagValue": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string | Avatar URL. |
| `dateCreated` | date | User creation timestamp, when present. |
| `email` | string | User email address. |
| `hash` | string | Sentry user hash. |
| `id` | string | User identifier, when Sentry provides one. |
| `identifier` | string | Sentry user identifier. |
| `ipAddress` | string | User IP address, when present. |
| `name` | string | User display name. |
| `tagValue` | string | Sentry user tag value. |
| `username` | string | Username. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /projects/:organization_id_or_slug/:project_id_or_slug/users/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-users.md) for the provider-specific parameters and requirements.

