# Postmark: Reactivate Bounce

Reactivates a bounce in Postmark.

```
PUT https://connect.mindcloud.co/v1/universal/postmark/latest/actions/reactivate-bounce
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/reactivate-bounce" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bounceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/reactivate-bounce', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bounceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bounceId` | string | yes | The Postmark bounce ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Bounce": {
        "CanActivate": true,
        "Email": "ava@example.com",
        "ID": "string",
        "Inactive": true,
        "MessageID": "string",
        "Type": "string"
      },
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Bounce` | object |  |
| `Bounce.CanActivate` | boolean |  |
| `Bounce.Email` | string |  |
| `Bounce.ID` | string |  |
| `Bounce.Inactive` | boolean |  |
| `Bounce.MessageID` | string |  |
| `Bounce.Type` | string |  |
| `Message` | string |  |

## Native endpoint

Through the native Postmark API, this operation is `PUT /bounces/:bounceId/activate` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reactivate-bounce.md) for the provider-specific parameters and requirements.

