# MailerSend: List Domain Recipients



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-domain-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-domain-recipients?connectionId=$CONNECTION_ID&domainId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-domain-recipients?${params}`, {
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
| `domainId` | string | yes | ID of the MailerSend domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": "string",
      "email": "ava@example.com",
      "id": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Recipient creation timestamp. |
| `deletedAt` | string | Recipient deletion timestamp when present. |
| `email` | string | Recipient email address. |
| `id` | string | MailerSend recipient ID. |
| `updatedAt` | string | Recipient update timestamp. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /domains/:domain_id/recipients` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domain-recipients.md) for the provider-specific parameters and requirements.

