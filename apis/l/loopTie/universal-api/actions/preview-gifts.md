# Loop & Tie: Preview Gifts

Creates gift preview links in Loop & Tie.

```
POST https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/preview-gifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop & Tie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/preview-gifts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopTie/latest/actions/preview-gifts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `giftCollection` | string | no | Collection name, such as $50. |
| `giftCollectionId` | string | no | Collection to preview. |
| `giftDeliveryMethod` | string | no | Delivery method, such as link or email. |
| `giftEmail` | string | no | Recipient email address. |
| `giftFrom` | string | no | Sender name shown to the recipient. |
| `giftFromName` | string | no | Sender display name. |
| `giftMessage` | string | no | Gift message. |
| `giftName` | string | no | Recipient display name. |
| `teamId` | string | no | The Loop & Tie team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The generated preview links and preview metadata. |

## Native endpoint

Through the native Loop & Tie API, this operation is `POST /teams/:teamId/previews` (base URL `https://api.loopandtie.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-gifts.md) for the provider-specific parameters and requirements.

