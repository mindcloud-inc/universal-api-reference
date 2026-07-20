# ChatDaddy: Update Messages in Bulk

Performs bulk actions on messages in ChatDaddy.

```
PUT https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-messages-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-messages-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "cancel"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-messages-in-bulk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "cancel"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | yes | Bulk message action to perform. Default: `cancel`. |
| `status` | string | no | Message status bucket to target for the bulk action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the bulk message action completed successfully. |

## Native endpoint

Through the native ChatDaddy API, this operation is `POST /messages/bulk-action` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-messages-in-bulk.md) for the provider-specific parameters and requirements.

