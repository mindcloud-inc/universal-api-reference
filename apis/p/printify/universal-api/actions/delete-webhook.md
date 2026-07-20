# Printify: Delete Webhook

Deletes a webhook from Printify.

```
DELETE https://connect.mindcloud.co/v1/universal/printify/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/printify/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&host=example.com&shop_id=27141936&webhook_id=69d9636798c77b61480a2daa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "host": "example.com",
  "shop_id": "27141936",
  "webhook_id": "69d9636798c77b61480a2daa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/delete-webhook?${params}`, {
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
| `host` | string | yes | Expected host of the webhook URL. Default: `example.com`. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |
| `webhook_id` | string | yes | Printify webhook id. Default: `69d9636798c77b61480a2daa`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Printify API, this operation is `DELETE /shops/:shop_id/webhooks/:webhook_id.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

