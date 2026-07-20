# TouchBasePro: Update SMS List Webhook

Updates an existing SMS list webhook in TouchBasePro.

```
PUT https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/update-sms-list-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/update-sms-list-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/update-sms-list-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isActive": true,
      "url": "https://example.com",
      "webhookType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `url` | string |  |
| `webhookType` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `PUT /sms/lists/{listId}/webhooks/{webhookId}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sms-list-webhook.md) for the provider-specific parameters and requirements.

