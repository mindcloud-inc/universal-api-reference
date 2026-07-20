# Sender: Delete Subscriber



```
DELETE https://connect.mindcloud.co/v1/universal/sender/latest/actions/delete-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sender/latest/actions/delete-subscriber?connectionId=$CONNECTION_ID&subscribers%5B%5D=user%40example.com%2Canother%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscribers[]": "user@example.com,another@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/delete-subscriber?${params}`, {
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
| `subscribers[]` | array<string> | yes | Array of subscriber emails to be deleted. Example: `user@example.com,another@example.com`. |
| `conditions` | string | no | Select subscribers in bulk. Cannot be combined with subscribers. Example: `status=UNSUBSCRIBED`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleteInstance": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleteInstance` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Sender API, this operation is `DELETE /subscribers` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber.md) for the provider-specific parameters and requirements.

