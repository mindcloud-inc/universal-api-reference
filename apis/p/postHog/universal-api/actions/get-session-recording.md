# PostHog: Get Session Recording

Retrieves a session recording from a PostHog project.

```
GET https://connect.mindcloud.co/v1/universal/postHog/latest/actions/get-session-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostHog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/get-session-recording?connectionId=$CONNECTION_ID&id=string&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postHog/latest/actions/get-session-recording?${params}`, {
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
| `id` | string | yes |  |
| `project_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeSeconds": 1,
      "activityScore": 1,
      "clickCount": 1,
      "consoleErrorCount": 1,
      "consoleLogCount": 1,
      "consoleWarnCount": 1,
      "distinctId": "string",
      "endTime": "string",
      "expiryTime": "string",
      "id": "string",
      "inactiveSeconds": 1,
      "keypressCount": 1,
      "mouseActivityCount": 1,
      "ongoing": true,
      "person": {
        "createdAt": "string",
        "distinctIds": [
          "string"
        ],
        "id": 1,
        "name": "Ava Chen",
        "properties": {},
        "uuid": "string"
      },
      "recordingDuration": 1,
      "recordingTtl": 1,
      "retentionPeriodDays": 1,
      "snapshotLibrary": "string",
      "snapshotSource": "string",
      "startTime": "string",
      "startUrl": "https://example.com",
      "viewed": true,
      "viewers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSeconds` | number |  |
| `activityScore` | number |  |
| `clickCount` | number |  |
| `consoleErrorCount` | number |  |
| `consoleLogCount` | number |  |
| `consoleWarnCount` | number |  |
| `distinctId` | string |  |
| `endTime` | string |  |
| `expiryTime` | string |  |
| `id` | string |  |
| `inactiveSeconds` | number |  |
| `keypressCount` | number |  |
| `mouseActivityCount` | number |  |
| `ongoing` | boolean |  |
| `person.createdAt` | string |  |
| `person.distinctIds[]` | string |  |
| `person.id` | number |  |
| `person.name` | string |  |
| `person.properties` | object |  |
| `person.uuid` | string |  |
| `recordingDuration` | number |  |
| `recordingTtl` | number |  |
| `retentionPeriodDays` | number |  |
| `snapshotLibrary` | string |  |
| `snapshotSource` | string |  |
| `startTime` | string |  |
| `startUrl` | string |  |
| `viewed` | boolean |  |
| `viewers[]` | string |  |

## Native endpoint

Through the native PostHog API, this operation is `GET /projects/:project_id/session_recordings/:id/` (base URL `https://us.posthog.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-recording.md) for the provider-specific parameters and requirements.

