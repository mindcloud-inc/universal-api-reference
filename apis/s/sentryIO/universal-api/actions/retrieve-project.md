# Sentry IO: Retrieve Project

Retrieves a project from Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-project?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&projectIdOrSlug=my-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "projectIdOrSlug": "my-project"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-project?${params}`, {
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "organization": {},
      "platform": "string",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date | Project creation timestamp. |
| `id` | string | Project identifier. |
| `name` | string | Project name. |
| `organization` | object | Owning organization. |
| `platform` | string | Project platform. |
| `slug` | string | Project slug. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /projects/:organization_id_or_slug/:project_id_or_slug/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-project.md) for the provider-specific parameters and requirements.

