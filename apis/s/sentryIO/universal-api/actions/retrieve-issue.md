# Sentry IO: Retrieve Issue

Retrieves an issue from Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-issue?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&issueId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "issueId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-issue?${params}`, {
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
| `issueId` | string | yes | The Sentry issue ID. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "level": "string",
      "permalink": "https://example.com",
      "project": {},
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
| `id` | string | Sentry issue identifier. |
| `level` | string | Issue severity level. |
| `permalink` | string | Issue URL. |
| `project` | object | Associated Sentry project. |
| `shortId` | string | Human-readable issue short ID. |
| `status` | string | Issue status. |
| `title` | string | Issue title. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/issues/:issue_id/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-issue.md) for the provider-specific parameters and requirements.

