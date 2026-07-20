# SMSGlobal: List Dedicated Numbers

Retrieves dedicated numbers from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-dedicated-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-dedicated-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-dedicated-numbers?${params}`, {
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
      "dedicatedNumbers": [
        {
          "autoReplyMessage": "string",
          "autoReplyOrigin": "string",
          "emailAddress": "ava@example.com",
          "httpCallbackUrl": "https://example.com",
          "id": 1,
          "isAutoReplyEnabled": true,
          "msisdn": "string",
          "type": "string",
          "userId": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dedicatedNumbers[].autoReplyMessage` | string | Automatic reply message. |
| `dedicatedNumbers[].autoReplyOrigin` | string | Origin used for the automatic reply. |
| `dedicatedNumbers[].emailAddress` | string | Email destination for incoming SMS. |
| `dedicatedNumbers[].httpCallbackUrl` | string | HTTP callback URL for incoming SMS. |
| `dedicatedNumbers[].id` | number | Dedicated number identifier. |
| `dedicatedNumbers[].isAutoReplyEnabled` | boolean | Whether auto reply messages are enabled. |
| `dedicatedNumbers[].msisdn` | string | Dedicated mobile number. |
| `dedicatedNumbers[].type` | string | Incoming message handling mode. |
| `dedicatedNumbers[].userId` | number | Owner account identifier. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/dedicated-number` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dedicated-numbers.md) for the provider-specific parameters and requirements.

