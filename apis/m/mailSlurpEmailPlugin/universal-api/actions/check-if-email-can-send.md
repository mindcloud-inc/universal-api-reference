# MailSlurp Email Plugin: Check If Email Can Send

Checks whether MailSlurp can send an email.

```
GET https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/check-if-email-can-send
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/check-if-email-can-send?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/check-if-email-can-send?${params}`, {
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
      "isSendingPermitted": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isSendingPermitted` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `POST /emails/can-send` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-if-email-can-send.md) for the provider-specific parameters and requirements.

