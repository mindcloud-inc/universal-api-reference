# Kanban Zone: List Webhooks

Retrieves webhooks from Kanban Zone.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&board=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "board": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-webhooks?${params}`, {
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
| `board` | string | yes | The public ID of the board. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board": "string",
      "description": "string",
      "enabled": true,
      "events": [
        "string"
      ],
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board` | string |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `events` | array<string> |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `GET /webhooks` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

