# eSign Genie: List All Webhook Channels

Retrieves webhook channels from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-all-webhook-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-all-webhook-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/list-all-webhook-channels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "templatesList": [
        {
          "channelId": 1,
          "channelName": "Ava Chen",
          "eventsSubscribedMap": {
            "folderSent": true
          },
          "status": "string",
          "webhookLevel": "string",
          "webhookUrl": "https://example.com"
        }
      ],
      "totalChannel": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `templatesList[].channelId` | number |  |
| `templatesList[].channelName` | string |  |
| `templatesList[].eventsSubscribedMap.folderSent` | boolean |  |
| `templatesList[].status` | string |  |
| `templatesList[].webhookLevel` | string |  |
| `templatesList[].webhookUrl` | string |  |
| `totalChannel` | number |  |

## Native endpoint

Through the native eSign Genie API, this operation is `GET /webhook/channellist` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-webhook-channels.md) for the provider-specific parameters and requirements.

