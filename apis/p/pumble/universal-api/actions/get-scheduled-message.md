# Pumble: Get Scheduled Message

Retrieves a scheduled message from Pumble by ID.

```
GET https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-scheduled-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-scheduled-message?connectionId=$CONNECTION_ID&scheduledMessageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduledMessageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-scheduled-message?${params}`, {
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
| `scheduledMessageId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "channelId": "string",
      "id": "string",
      "sendAt": 1,
      "text": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `channelId` | string |  |
| `id` | string |  |
| `sendAt` | number |  |
| `text` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Pumble API, this operation is `GET /fetchScheduledMessage` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scheduled-message.md) for the provider-specific parameters and requirements.

