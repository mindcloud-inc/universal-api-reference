# Vero: Retrieve Message

Retrieves a message record from Vero.

```
GET https://connect.mindcloud.co/v1/universal/vero/latest/actions/retrieve-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vero/latest/actions/retrieve-message?connectionId=$CONNECTION_ID&id=message_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "message_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vero/latest/actions/retrieve-message?${params}`, {
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
| `id` | string | yes | The message identifier. Default: `message_example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "id": "string",
      "object": "string",
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string | Owning campaign identifier. |
| `id` | string | Message identifier. |
| `object` | string | Resource type. |
| `provider` | string | Delivery provider. |

## Native endpoint

Through the native Vero API, this operation is `GET /api/v4/messages/:id` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-message.md) for the provider-specific parameters and requirements.

