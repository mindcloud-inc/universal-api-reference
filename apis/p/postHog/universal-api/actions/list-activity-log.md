# PostHog: List Activity Log

Retrieves activity log entries from a PostHog project.

```
GET https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-activity-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostHog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-activity-log?connectionId=$CONNECTION_ID&project_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-activity-log?${params}`, {
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
| `project_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity": "string",
      "createdAt": "string",
      "detail": {
        "changes": [
          {
            "action": "string",
            "after": {},
            "before": {},
            "field": "string",
            "type": "string"
          }
        ],
        "context": {},
        "name": "Ava Chen",
        "shortId": "string",
        "trigger": {},
        "type": "string"
      },
      "id": "string",
      "isSystem": true,
      "itemId": "string",
      "organizationId": "string",
      "scope": "string",
      "unread": true,
      "user": {
        "distinctId": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "hedgehogConfig": {},
        "id": 1,
        "isEmailVerified": true,
        "lastName": "Chen",
        "roleAtOrganization": "string",
        "uuid": "string"
      },
      "wasImpersonated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity` | string |  |
| `createdAt` | string |  |
| `detail.changes[].action` | string |  |
| `detail.changes[].after` | object |  |
| `detail.changes[].before` | object |  |
| `detail.changes[].field` | string |  |
| `detail.changes[].type` | string |  |
| `detail.context` | object |  |
| `detail.name` | string |  |
| `detail.shortId` | string |  |
| `detail.trigger` | object |  |
| `detail.type` | string |  |
| `id` | string |  |
| `isSystem` | boolean |  |
| `itemId` | string |  |
| `organizationId` | string |  |
| `scope` | string |  |
| `unread` | boolean |  |
| `user.distinctId` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.hedgehogConfig` | object |  |
| `user.id` | number |  |
| `user.isEmailVerified` | boolean |  |
| `user.lastName` | string |  |
| `user.roleAtOrganization` | string |  |
| `user.uuid` | string |  |
| `wasImpersonated` | boolean |  |

## Native endpoint

Through the native PostHog API, this operation is `GET /projects/:projectId/activity_log/` (base URL `https://us.posthog.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activity-log.md) for the provider-specific parameters and requirements.

