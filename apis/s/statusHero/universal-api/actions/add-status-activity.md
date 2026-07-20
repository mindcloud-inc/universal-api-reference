# Status Hero: Add status activity



```
POST https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-status-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-status-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps@mindcloud.co",
  "source": "MindCloud",
  "description": "Updated integration task"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-status-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps@mindcloud.co",
    "source": "MindCloud",
    "description": "Updated integration task"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address for the associated team member. Must match a Status Hero member. Example: `apps@mindcloud.co`. |
| `source` | string | yes | The external activity source name, such as a board or repository. Example: `MindCloud`. |
| `description` | string | yes | Brief activity description. Simple HTML markup is accepted by Status Hero. Example: `Updated integration task`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | no | Optional external URL for the activity source. Example: `https://example.com/activity`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "htmlDescription": "string",
      "id": "string",
      "kind": "string",
      "statusId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `htmlDescription` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `statusId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Status Hero API, this operation is `POST /status_activities` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-status-activity.md) for the provider-specific parameters and requirements.

