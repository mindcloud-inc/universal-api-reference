# SMS.to: Estimate Personalized Message

Retrieves a cost estimate for personalized SMS messages.

```
GET https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/estimate-personalized-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/estimate-personalized-message?connectionId=$CONNECTION_ID&messages%5B%5D=%5Bobject%20Object%5D&messages%5B%5D.message=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messages[]": "[object Object]",
  "messages[].message": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/estimate-personalized-message?${params}`, {
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
| `messages[]` | array<object> | yes | Array of message objects with recipient phone numbers. |
| `messages[].message` | string | yes | Your message for the specified phone number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[].to` | string | no | The recipient phone number. |
| `senderId` | string | no | The displayed value of who sent the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactCount": 1,
      "estimatedCost": 1,
      "invalidCount": 1,
      "maxSmsCount": 1,
      "minSmsCount": 1,
      "smsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactCount` | number |  |
| `estimatedCost` | number |  |
| `invalidCount` | number |  |
| `maxSmsCount` | number |  |
| `minSmsCount` | number |  |
| `smsCount` | number |  |

## Native endpoint

Through the native SMS.to API, this operation is `POST /sms/estimate` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-personalized-message.md) for the provider-specific parameters and requirements.

