# Email Hippo: Verify Email (MORE V2)

Verifies an email address with Email Hippo MORE V2.

```
GET https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/verify-email-morev2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Email Hippo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/verify-email-morev2?connectionId=$CONNECTION_ID&emailAddress=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/verify-email-morev2?${params}`, {
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
| `emailAddress` | string | yes | The email address to verify. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disposable": true,
      "domain": "string",
      "duration": 1,
      "email": "ava@example.com",
      "free": true,
      "mailServerLocation": "string",
      "reason": "string",
      "result": "string",
      "role": true,
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disposable` | boolean |  |
| `domain` | string |  |
| `duration` | number |  |
| `email` | string |  |
| `free` | boolean |  |
| `mailServerLocation` | string |  |
| `reason` | string |  |
| `result` | string |  |
| `role` | boolean |  |
| `user` | string |  |

## Native endpoint

Through the native Email Hippo API, this operation is `GET https://api1.27hub.com/api/emh/a/v2?k={{credentials.apiKey}}&e=:emailAddress` (base URL `https://api.hippoapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-morev2.md) for the provider-specific parameters and requirements.

