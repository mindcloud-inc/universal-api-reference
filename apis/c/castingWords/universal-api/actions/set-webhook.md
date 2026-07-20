# CastingWords: Set Webhook

Updates webhook settings in CastingWords.

```
PUT https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/set-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CastingWords `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/set-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhook": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castingWords/latest/actions/set-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhook": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhook` | string | yes | HTTP or HTTPS endpoint to receive CastingWords webhook events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhook": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhook` | string | Registered webhook URL for the account. |

## Native endpoint

Through the native CastingWords API, this operation is `POST webhook` (base URL `https://castingwords.com/store/API4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-webhook.md) for the provider-specific parameters and requirements.

