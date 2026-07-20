# MailSlurp Email Plugin: Get Email

Retrieves a hydrated email from MailSlurp.

```
GET https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/get-email?${params}`, {
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
| `emailId` | string | no | The MailSlurp email ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyExcerpt": "string",
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyExcerpt` | string |  |
| `createdAt` | string |  |
| `from` | string |  |
| `id` | string |  |
| `inboxId` | string |  |
| `read` | boolean |  |
| `subject` | string |  |
| `to` | array<string> |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `GET /emails/:emailId` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

