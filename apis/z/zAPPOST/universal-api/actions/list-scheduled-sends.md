# ZAP POST: List Scheduled Sends

Retrieves scheduled sends from ZAP POST.

```
GET https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-scheduled-sends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZAP POST `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-scheduled-sends?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zAPPOST/latest/actions/list-scheduled-sends?${params}`, {
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
      "Id": "string",
      "PaperStockName": "Ava Chen",
      "SendDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | string | Scheduled send identifier returned by the Scheduled Sends endpoint. |
| `PaperStockName` | string | Paper stock label for the scheduled send. |
| `SendDate` | date | Scheduled mail date for the send. |

## Native endpoint

Through the native ZAP POST API, this operation is `GET /api/v1/ScheduledSends` (base URL `https://api.zappost.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scheduled-sends.md) for the provider-specific parameters and requirements.

