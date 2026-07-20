# LeadTable: Detach webhook



```
DELETE https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/detach-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/detach-webhook?connectionId=$CONNECTION_ID&topic=Change%20status&layer=Agency&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "Change status",
  "layer": "Agency",
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/detach-webhook?${params}`, {
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
| `topic` | list | yes | Webhook topic to detach. One of: `Change status`, `Delete lead`, `New lead`, `New table`, `Update lead`. |
| `layer` | list | yes | Scope level where the webhook is attached. One of: `Agency`, `Customer`, `Table`. |
| `url` | string | yes | The exact webhook URL that should be detached. |
| `campaignID` | string | no | Campaign ID when detaching a table-level webhook. |
| `customerID` | string | no | Customer ID when detaching a customer-level webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "removed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `removed` | boolean | Whether the webhook was detached. |

## Native endpoint

Through the native LeadTable API, this operation is `POST /removeWebhook` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-webhook.md) for the provider-specific parameters and requirements.

