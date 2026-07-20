# Sozuri (Kenya) SMS: Delete Subscriber

Deactivates a premium SMS subscriber in Sozuri.

```
DELETE https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/delete-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sozuri (Kenya) SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/delete-subscriber?connectionId=$CONNECTION_ID&shortcode=string&keyword=string&number=string&network=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortcode": "string",
  "keyword": "string",
  "number": "string",
  "network": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/delete-subscriber?${params}`, {
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
| `shortcode` | string | yes | The premium shortcode for the service. |
| `keyword` | string | yes | The premium service keyword. |
| `number` | string | yes | The subscriber phone number in E.164 format. |
| `network` | string | yes | The subscriber mobile network, for example safaricom. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | array<object> |  |

## Native endpoint

Through the native Sozuri (Kenya) SMS API, this operation is `POST /premium` (base URL `https://sozuri.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber.md) for the provider-specific parameters and requirements.

