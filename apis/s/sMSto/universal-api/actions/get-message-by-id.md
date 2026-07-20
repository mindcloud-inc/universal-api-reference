# SMS.to: Get Message by ID

Retrieves a sent message by ID from SMS.to.

```
GET https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-message-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-message-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/get-message-by-id?${params}`, {
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
| `id` | string | yes | Message identifier. |

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

Through the native SMS.to API, this operation is `GET /message/:id` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-by-id.md) for the provider-specific parameters and requirements.

