# Sentry IO: List Organization Issues

Retrieves issues from a Sentry IO organization.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-organization-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-organization-issues?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-organization-issues?${params}`, {
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
| `query` | string | no | Optional Sentry structured search query. Leave blank for Sentry's default unresolved issue query; pass an empty query value to request all results. Example: `is:unresolved`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | no | Optional Sentry project ID. Sentry also accepts -1 for all available projects. Example: `-1`. |
| `statsPeriod` | string | no | Optional time range such as 24h, 7d, or 14d for issue stats. Example: `24h`. |
| `sort` | list | no | Optional Sentry issue sort such as date, freq, inbox, new, recommended, trends, or user. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `cursor` | string | no | Optional Sentry pagination cursor from the Link header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": "string",
      "firstSeen": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "level": "string",
      "permalink": "https://example.com",
      "project": {},
      "shortId": "string",
      "status": "string",
      "title": "string",
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | string | Event count for the issue |
| `firstSeen` | date | First seen timestamp |
| `id` | string | Sentry issue ID |
| `lastSeen` | date | Last seen timestamp |
| `level` | string | Issue severity level |
| `permalink` | string | Sentry issue URL |
| `project` | object | Project summary for the issue |
| `shortId` | string | Human-readable short issue ID |
| `status` | string | Issue status |
| `title` | string | Issue title |
| `userCount` | number | Number of users affected |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/issues/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-issues.md) for the provider-specific parameters and requirements.

