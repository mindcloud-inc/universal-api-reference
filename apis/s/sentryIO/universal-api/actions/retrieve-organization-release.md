# Sentry IO: Retrieve Organization Release

Retrieves an organization release from Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-organization-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-organization-release?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&version=frontend%40abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "version": "frontend@abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-organization-release?${params}`, {
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
| `version` | string | yes | The Sentry release version identifier. Example: `frontend@abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": [
        {}
      ],
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateReleased": "2026-05-07T12:00:00.000Z",
      "projects": [
        {}
      ],
      "shortVersion": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors` | array<object> | Release authors. |
| `dateCreated` | date | Release creation timestamp. |
| `dateReleased` | date | Release timestamp. |
| `projects` | array<object> | Projects in the release. |
| `shortVersion` | string | Short release version. |
| `version` | string | Release version. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/releases/:version/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-organization-release.md) for the provider-specific parameters and requirements.

