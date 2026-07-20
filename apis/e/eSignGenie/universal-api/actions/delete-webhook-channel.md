# eSign Genie: Delete Webhook Channel

Deletes a webhook channel from eSign Genie.

```
DELETE https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/delete-webhook-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/delete-webhook-channel?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/delete-webhook-channel?${params}`, {
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
      "webhookChannelsDeletedSuccessfully": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `webhookChannelsDeletedSuccessfully[]` | number |  |

## Native endpoint

Through the native eSign Genie API, this operation is `POST /webhook/deletechannels` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-channel.md) for the provider-specific parameters and requirements.

