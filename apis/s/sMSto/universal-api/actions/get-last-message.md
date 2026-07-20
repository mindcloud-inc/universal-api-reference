# SMS.to: Get Last Message

Retrieves the most recent sent message from SMS.to.

```
GET https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-message?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-message?${params}`, {
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
      "callbackUrl": "https://example.com",
      "campaignId": "string",
      "cost": 1,
      "createdAt": "string",
      "failedReason": "string",
      "id": "string",
      "internalFailedReason": "string",
      "isApi": true,
      "message": "string",
      "scheduledFor": "string",
      "senderId": "string",
      "sentAt": "string",
      "smsCount": 1,
      "status": "string",
      "timezone": "string",
      "to": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `campaignId` | string |  |
| `cost` | number |  |
| `createdAt` | string |  |
| `failedReason` | string |  |
| `id` | string |  |
| `internalFailedReason` | string |  |
| `isApi` | boolean |  |
| `message` | string |  |
| `scheduledFor` | string |  |
| `senderId` | string |  |
| `sentAt` | string |  |
| `smsCount` | number |  |
| `status` | string |  |
| `timezone` | string |  |
| `to` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native SMS.to API, this operation is `GET /v2/last/message` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-last-message.md) for the provider-specific parameters and requirements.

