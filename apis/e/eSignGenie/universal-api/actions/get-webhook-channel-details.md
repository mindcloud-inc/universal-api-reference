# eSign Genie: Get Webhook Channel Details

Retrieves webhook channel details from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-webhook-channel-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-webhook-channel-details?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/get-webhook-channel-details?${params}`, {
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
| `channelId` | number | yes | The Foxit eSign webhook channel ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {
        "channelId": 1,
        "channelName": "Ava Chen",
        "eventsSubscribedMap": {
          "folderSent": true
        },
        "status": "string",
        "webhookLevel": "string",
        "webhookUrl": "https://example.com"
      },
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel.channelId` | number |  |
| `channel.channelName` | string |  |
| `channel.eventsSubscribedMap.folderSent` | boolean |  |
| `channel.status` | string |  |
| `channel.webhookLevel` | string |  |
| `channel.webhookUrl` | string |  |
| `result` | string |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /webhook/mychannel` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-channel-details.md) for the provider-specific parameters and requirements.

