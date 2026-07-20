# Sentry IO: Retrieve Team

Retrieves a team from Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-team?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&teamIdOrSlug=my-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "teamIdOrSlug": "my-team"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-team?${params}`, {
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "projects": [
        {}
      ],
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date | Team creation timestamp. |
| `id` | string | Team identifier. |
| `name` | string | Team name. |
| `projects` | array<object> | Projects associated with the team. |
| `slug` | string | Team slug. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /teams/:organization_id_or_slug/:team_id_or_slug/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-team.md) for the provider-specific parameters and requirements.

