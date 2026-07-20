# ChipBot: Delete Video



```
DELETE https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/delete-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/delete-video?connectionId=$CONNECTION_ID&videoExpId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoExpId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/delete-video?${params}`, {
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
| `videoExpId` | string | yes | The video experience identifier, for example videxp_xxx. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "acknowledged": true,
          "deletedCount": 1
        }
      ],
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Delete-operation results. |
| `data[].acknowledged` | boolean | Deletion acknowledgment flag. |
| `data[].deletedCount` | number | Number of deleted records for the affected store. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `DELETE /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video.md) for the provider-specific parameters and requirements.

