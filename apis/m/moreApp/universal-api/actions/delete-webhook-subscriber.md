# MoreApp: Delete Webhook Subscriber

Deletes a webhook subscriber from MoreApp.

```
DELETE https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-webhook-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-webhook-subscriber?connectionId=$CONNECTION_ID&customerId=209321&subscriberId=69bc44ef924bd75a32933a4a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321",
  "subscriberId": "69bc44ef924bd75a32933a4a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/delete-webhook-subscriber?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `subscriberId` | string | yes | MoreApp subscriber identifier. Default: `69bc44ef924bd75a32933a4a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "secret": "string",
      "status": "string",
      "type": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `secret` | string |  |
| `status` | string |  |
| `type` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native MoreApp API, this operation is `DELETE /api/v1.0/webhooks/customer/{{customerId}}/subscribers/{{subscriberId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-subscriber.md) for the provider-specific parameters and requirements.

