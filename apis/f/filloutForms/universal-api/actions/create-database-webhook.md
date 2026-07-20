# Fillout Forms: Create Database Webhook

Creates a database webhook in Fillout.

```
POST https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-database-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-database-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "base_abc123",
  "url": "https://your-server.com/webhooks/fillout",
  "events[]": "record.created,record.updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-database-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "base_abc123",
    "url": "https://your-server.com/webhooks/fillout",
    "events[]": "record.created,record.updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The unique identifier of the database. Example: `base_abc123`. |
| `url` | string | yes | The URL to receive webhook POST requests. Example: `https://your-server.com/webhooks/fillout`. |
| `events[]` | array<string> | yes | Array of event types to subscribe to. Example: `record.created,record.updated`. |
| `tableId` | string | no | Optional table ID to filter events. Omit to receive events from all tables. Example: `tbl_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "secret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Webhook identifier. |
| `secret` | string | Webhook signing secret returned once at creation. |

## Native endpoint

Through the native Fillout Forms API, this operation is `POST https://tables.fillout.com/api/v1/bases/:databaseId/webhooks` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database-webhook.md) for the provider-specific parameters and requirements.

