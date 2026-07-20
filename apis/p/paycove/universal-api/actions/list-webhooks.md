# Paycove: List Webhooks

Retrieves webhook subscriptions from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-webhooks?${params}`, {
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
      "accountId": 1,
      "createdAt": "string",
      "destinationApp": "string",
      "event": "string",
      "id": 1,
      "notificationTemplateId": {},
      "sendTo": {},
      "signingKey": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `createdAt` | string |  |
| `destinationApp` | string |  |
| `event` | string |  |
| `id` | number |  |
| `notificationTemplateId` | object |  |
| `sendTo` | object |  |
| `signingKey` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Paycove API, this operation is `GET hooks` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

