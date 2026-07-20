# Sentry IO: Resolve Event ID

Resolves a Sentry IO event ID to event details.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/resolve-event-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/resolve-event-id?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org&eventId=9fac2ceed9344f2bbfdd1fdacb0ed9b1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org",
  "eventId": "9fac2ceed9344f2bbfdd1fdacb0ed9b1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/resolve-event-id?${params}`, {
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
| `eventId` | string | yes | The Sentry event ID to resolve. Example: `9fac2ceed9344f2bbfdd1fdacb0ed9b1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": {},
      "eventId": "string",
      "groupId": "string",
      "organizationSlug": "string",
      "projectSlug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | object | Resolved event object. |
| `eventId` | string | Resolved event ID. |
| `groupId` | string | Associated issue group ID, when present. |
| `organizationSlug` | string | Organization slug for the event. |
| `projectSlug` | string | Project slug for the event. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/eventids/:event_id/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-event-id.md) for the provider-specific parameters and requirements.

