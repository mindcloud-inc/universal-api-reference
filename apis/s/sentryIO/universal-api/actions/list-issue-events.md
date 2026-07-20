# Sentry IO: List Issue Events

Retrieves events for an issue in Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-issue-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-issue-events?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&issueId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "issueId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-issue-events?${params}`, {
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
| `issueId` | string | yes | The Sentry issue ID whose events should be listed. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/issues/:issue_id/events/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issue-events.md) for the provider-specific parameters and requirements.

