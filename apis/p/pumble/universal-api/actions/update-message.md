# Pumble: Update Message

Updates the text of a Pumble message.

```
PUT https://connect.mindcloud.co/v1/universal/pumble/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pumble/latest/actions/update-message', {
  method: 'PUT',
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
| `channelId` | string | no |  |
| `messageId` | string | no |  |
| `text` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pumble API returns.

## Native endpoint

Through the native Pumble API, this operation is `POST /editMessage` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

