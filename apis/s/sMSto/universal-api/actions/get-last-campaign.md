# SMS.to: Get Last Campaign

Retrieves the most recent campaign from SMS.to.

```
GET https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-campaign?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-last-campaign?${params}`, {
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
      "canceledAt": "string",
      "createdAt": "string",
      "deliveredMessages": 1,
      "estimatedCost": 1,
      "failedMessages": 1,
      "id": "string",
      "isApi": 1,
      "listId": 1,
      "message": "string",
      "pendingMessages": 1,
      "scheduledFor": "string",
      "senderId": "string",
      "sentMessages": 1,
      "smsCount": 1,
      "status": "string",
      "type": "string",
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `canceledAt` | string |  |
| `createdAt` | string |  |
| `deliveredMessages` | number |  |
| `estimatedCost` | number |  |
| `failedMessages` | number |  |
| `id` | string |  |
| `isApi` | number |  |
| `listId` | number |  |
| `message` | string |  |
| `pendingMessages` | number |  |
| `scheduledFor` | string |  |
| `senderId` | string |  |
| `sentMessages` | number |  |
| `smsCount` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native SMS.to API, this operation is `GET /v2/last/campaign` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-last-campaign.md) for the provider-specific parameters and requirements.

