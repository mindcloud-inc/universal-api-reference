# SendSafely: Update Recipient



```
PUT https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/update-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/update-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/update-recipient', {
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
      "approvalRequired": true,
      "checkForPublicKeys": true,
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "isPackageOwner": true,
      "phonenumbers": [
        {}
      ],
      "recipientId": "string",
      "response": "string",
      "roleName": "Ava Chen",
      "smsAuth": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalRequired` | boolean |  |
| `checkForPublicKeys` | boolean |  |
| `email` | string |  |
| `fullName` | string |  |
| `isPackageOwner` | boolean |  |
| `phonenumbers` | array<object> |  |
| `recipientId` | string |  |
| `response` | string |  |
| `roleName` | string |  |
| `smsAuth` | boolean |  |

## Native endpoint

Through the native SendSafely API, this operation is `POST /package/:packageId/recipient/:recipientId/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recipient.md) for the provider-specific parameters and requirements.

