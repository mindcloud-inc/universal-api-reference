# CloudContactAI: Get Campaign Message Stats



```
GET https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-campaign-message-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-campaign-message-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-campaign-message-stats?${params}`, {
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
| `campaignId` | string | no | The campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "error": 1,
      "incoming": 1,
      "pending": 1,
      "requeueable": 1,
      "segments": 1,
      "sending": 1,
      "sent": 1,
      "sentAt": "2026-05-07T12:00:00.000Z",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `error` | number |  |
| `incoming` | number |  |
| `pending` | number |  |
| `requeueable` | number |  |
| `segments` | number |  |
| `sending` | number |  |
| `sent` | number |  |
| `sentAt` | date |  |
| `total` | number |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `GET api/v2/messages/campaign/:campaignId/stats` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-message-stats.md) for the provider-specific parameters and requirements.

