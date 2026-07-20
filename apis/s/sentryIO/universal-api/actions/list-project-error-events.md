# Sentry IO: List Project Error Events

Retrieves error events from a Sentry IO project.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-project-error-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-project-error-events?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&projectIdOrSlug=my-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "projectIdOrSlug": "my-project"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-project-error-events?${params}`, {
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
      "culprit": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "eventID": "string",
      "groupID": "string",
      "id": "string",
      "message": "string",
      "metadata": {},
      "platform": "string",
      "projectID": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `culprit` | string | Event culprit. |
| `dateCreated` | date | Event creation timestamp. |
| `eventID` | string | Sentry event ID. |
| `groupID` | string | Associated issue group ID. |
| `id` | string | Event identifier. |
| `message` | string | Event message. |
| `metadata` | object | Event metadata. |
| `platform` | string | Event platform. |
| `projectID` | string | Project identifier. |
| `tags` | array<object> | Event tags. |
| `title` | string | Event title. |
| `user` | object | Event user context. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /projects/:organization_id_or_slug/:project_id_or_slug/events/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-error-events.md) for the provider-specific parameters and requirements.

