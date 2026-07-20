# MailerSend: List Activity



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-activity?connectionId=$CONNECTION_ID&domainId=string&dateFrom=string&dateTo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "string",
  "dateFrom": "string",
  "dateTo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-activity?${params}`, {
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
| `dateFrom` | string | yes | Start datetime for activity results in YYYY-MM-DD HH:mm:ss format. |
| `dateTo` | string | yes | End datetime for activity results in YYYY-MM-DD HH:mm:ss format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "email": {},
      "id": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Activity creation timestamp. |
| `email` | object | Email payload associated with the activity event. |
| `id` | string | MailerSend activity event ID. |
| `type` | string | Activity type such as sent, delivered, opened, or clicked. |
| `updatedAt` | string | Activity update timestamp. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /activity/:domain_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activity.md) for the provider-specific parameters and requirements.

