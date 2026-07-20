# MailSlurp Email Plugin: Wait For Matching Emails

Waits for MailSlurp emails that match the given filters.

```
GET https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/wait-for-matching-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/wait-for-matching-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/wait-for-matching-emails?${params}`, {
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
      "": [
        {
          "createdAt": "string",
          "from": "string",
          "id": "string",
          "inboxId": "string",
          "read": true,
          "subject": "string",
          "to": [
            "string"
          ]
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
| `[].createdAt` | string |  |
| `[].from` | string |  |
| `[].id` | string |  |
| `[].inboxId` | string |  |
| `[].read` | boolean |  |
| `[].subject` | string |  |
| `[].to` | array<string> |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `POST /waitForMatchingEmails` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/wait-for-matching-emails.md) for the provider-specific parameters and requirements.

