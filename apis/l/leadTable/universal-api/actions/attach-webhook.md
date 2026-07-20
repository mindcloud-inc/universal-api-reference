# LeadTable: Attach webhook



```
POST https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/attach-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/attach-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "topic": "Change status",
  "layer": "Agency"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/attach-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "topic": "Change status",
    "layer": "Agency"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignID` | string | no | Campaign ID when attaching a table-level webhook. |
| `customerID` | string | no | Customer ID when attaching a customer-level webhook. |
| `url` | string | yes | The webhook URL to attach. |
| `topic` | list | yes | Webhook topic to attach. One of: `Change status`, `Delete lead`, `New lead`, `New table`, `Update lead`. |
| `layer` | list | yes | Scope level where the webhook should be attached. One of: `Agency`, `Customer`, `Table`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalHookId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalHookId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native LeadTable API, this operation is `POST /attachWebhook` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-webhook.md) for the provider-specific parameters and requirements.

