# Loopy Loyalty: Send Message To All Cards



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/send-message-to-all-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/send-message-to-all-cards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cid": "5fcDywPejwj9QszwngBTKg",
  "message": "Thanks for being a loyal customer."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/send-message-to-all-cards', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cid": "5fcDywPejwj9QszwngBTKg",
    "message": "Thanks for being a loyal customer."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cid` | string | yes | Example: `5fcDywPejwj9QszwngBTKg`. |
| `message` | string | yes | Example: `Thanks for being a loyal customer.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the campaign-wide message was sent successfully. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /card/cid/:cid/push` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message-to-all-cards.md) for the provider-specific parameters and requirements.

