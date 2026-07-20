# Sentry IO: Resolve Short ID

Retrieves Sentry IO issue details by short ID.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/resolve-short-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/resolve-short-id?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&issueId=PROJECT-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "issueId": "PROJECT-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/resolve-short-id?${params}`, {
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
| `issueId` | string | yes | The short issue ID to resolve, such as PROJECT-123. Example: `PROJECT-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group": {},
      "groupId": "string",
      "organizationSlug": "string",
      "projectSlug": "string",
      "shortId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group` | object | Resolved issue group object. |
| `groupId` | string | Resolved issue group ID. |
| `organizationSlug` | string | Organization slug. |
| `projectSlug` | string | Project slug for the issue. |
| `shortId` | string | Short issue ID. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/shortids/:issue_id/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-short-id.md) for the provider-specific parameters and requirements.

