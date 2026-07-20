# Sentry IO: Update Issue

Updates an existing issue in Sentry IO.

```
PUT https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/update-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/update-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationIdOrSlug": "my-org",
  "issueId": "123456789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/update-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationIdOrSlug": "my-org",
    "issueId": "123456789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationIdOrSlug` | string | yes | The Sentry organization ID or slug. Example: `my-org`. |
| `issueId` | string | yes | The Sentry issue ID to update. Example: `123456789`. |
| `status` | list | no | New issue status: resolved, resolvedInNextRelease, unresolved, or ignored. One of: `0`, `1`, `2`, `3`. |
| `assignedTo` | string | no | Actor ID or username of the user or team to assign to the issue. |
| `isBookmarked` | boolean | no | Whether the invoking user has bookmarked the issue. |
| `isSubscribed` | boolean | no | Whether the invoking user is subscribed to issue notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {},
      "id": "string",
      "isBookmarked": true,
      "isSubscribed": true,
      "shortId": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | object | Assigned user or team, when present. |
| `id` | string | Sentry issue identifier. |
| `isBookmarked` | boolean | Whether the issue is bookmarked. |
| `isSubscribed` | boolean | Whether the caller is subscribed. |
| `shortId` | string | Human-readable issue short ID. |
| `status` | string | Issue status after update. |
| `title` | string | Issue title after update. |

## Native endpoint

Through the native Sentry IO API, this operation is `PUT /organizations/:organization_id_or_slug/issues/:issue_id/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-issue.md) for the provider-specific parameters and requirements.

