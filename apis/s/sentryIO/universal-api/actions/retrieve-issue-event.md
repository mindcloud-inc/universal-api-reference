# Sentry IO: Retrieve Issue Event

Retrieves an event from a Sentry IO issue.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-issue-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-issue-event?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&issueId=123456789&eventId=latest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "issueId": "123456789",
  "eventId": "latest"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-issue-event?${params}`, {
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
| `eventId` | string | yes | The event ID to retrieve, or latest, oldest, or recommended. Example: `latest`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contexts": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateReceived": "2026-05-07T12:00:00.000Z",
      "entries": [
        {}
      ],
      "eventID": "string",
      "groupID": "string",
      "id": "string",
      "message": "string",
      "metadata": {},
      "platform": "string",
      "projectID": "string",
      "release": {},
      "sdk": {},
      "tags": [
        {}
      ],
      "title": "string",
      "type": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contexts` | object | Event contexts. |
| `dateCreated` | date | Event creation timestamp. |
| `dateReceived` | date | Event received timestamp. |
| `entries` | array<object> | Event entry details. |
| `eventID` | string | Sentry event ID. |
| `groupID` | string | Associated issue group ID. |
| `id` | string | Event identifier. |
| `message` | string | Event message. |
| `metadata` | object | Event metadata. |
| `platform` | string | Event platform. |
| `projectID` | string | Project identifier. |
| `release` | object | Associated release object. |
| `sdk` | object | SDK metadata. |
| `tags` | array<object> | Event tags. |
| `title` | string | Event title. |
| `type` | string | Event type. |
| `user` | object | Event user context. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/issues/:issue_id/events/:event_id/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-issue-event.md) for the provider-specific parameters and requirements.

