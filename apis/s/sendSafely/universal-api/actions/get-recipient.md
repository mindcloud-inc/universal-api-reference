# SendSafely: Get Recipient



```
GET https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-recipient?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-recipient?${params}`, {
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

Through the native SendSafely API, this operation is `GET /package/:packageId/recipient/:recipientId/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient.md) for the provider-specific parameters and requirements.

