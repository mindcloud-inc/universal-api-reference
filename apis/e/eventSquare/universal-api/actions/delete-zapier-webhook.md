# EventSquare: Delete Zapier Webhook

Deletes a Zapier webhook from EventSquare.

```
DELETE https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/delete-zapier-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventSquare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/delete-zapier-webhook?connectionId=$CONNECTION_ID&type=0&url=https%3A%2F%2Fexample.com%2Fwebhooks%2Feventsquare" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "0",
  "url": "https://example.com/webhooks/eventsquare"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/delete-zapier-webhook?${params}`, {
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
| `type` | string | yes | The EventSquare trigger type for the webhook you want to delete. One of: `0`. |
| `url` | string | yes | The exact webhook URL to remove from EventSquare. Example: `https://example.com/webhooks/eventsquare`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Success status returned after the webhook is deleted. |

## Native endpoint

Through the native EventSquare API, this operation is `DELETE /1.0/integrations/zapier/triggers` (base URL `https://api.eventsquare.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-zapier-webhook.md) for the provider-specific parameters and requirements.

