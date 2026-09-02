# ClickUp: List Webhook

Lists a team webhooks in ClickUp for selected events.

```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-webhook?connectionId=$CONNECTION_ID&teamID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-webhook?${params}`, {
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
| `teamID` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "webhook": {
        "clientId": "string",
        "endpoint": "string",
        "events": [
          "string"
        ],
        "folderId": "string",
        "health": {
          "failCount": 1,
          "status": "string"
        },
        "id": "string",
        "listId": "string",
        "secret": "string",
        "spaceId": "string",
        "taskId": "string",
        "teamId": 1,
        "userid": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `webhook` | object |  |
| `webhook.clientId` | string |  |
| `webhook.endpoint` | string |  |
| `webhook.events` | array |  |
| `webhook.events[]` | string |  |
| `webhook.folderId` | string |  |
| `webhook.health` | object |  |
| `webhook.health.failCount` | number |  |
| `webhook.health.status` | string |  |
| `webhook.id` | string |  |
| `webhook.listId` | string |  |
| `webhook.secret` | string |  |
| `webhook.spaceId` | string |  |
| `webhook.taskId` | string |  |
| `webhook.teamId` | number |  |
| `webhook.userid` | number |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET team/:team_id/webhook` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook.md) for the provider-specific parameters and requirements.

