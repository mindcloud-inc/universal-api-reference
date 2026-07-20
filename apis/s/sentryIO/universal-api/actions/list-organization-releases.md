# Sentry IO: List Organization Releases

Retrieves releases from a Sentry IO organization.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-organization-releases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-organization-releases?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-organization-releases?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `dateCreated` | date | Release creation timestamp. |
| `dateReleased` | date | Release timestamp. |
| `projects` | array<object> | Projects in the release. |
| `shortVersion` | string | Short release version. |
| `version` | string | Release version. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/releases/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organization-releases.md) for the provider-specific parameters and requirements.

