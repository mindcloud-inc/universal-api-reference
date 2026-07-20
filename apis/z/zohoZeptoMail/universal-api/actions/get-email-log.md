# Zoho ZeptoMail: Get Email Log

Retrieves a specific email log from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/get-email-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/get-email-log?connectionId=$CONNECTION_ID&emailReference=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailReference": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/get-email-log?${params}`, {
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
| `emailReference` | string | yes | Unique email reference returned by ZeptoMail. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "bcc": "string",
        "cc": "string",
        "client_reference": "string",
        "from": "string",
        "is_delivered": true,
        "is_hb": true,
        "is_mailfailure": true,
        "is_sb": true,
        "mailagent_key": "string",
        "request_id": "string",
        "status": "string",
        "subject": "string",
        "to": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.bcc` | string |  |
| `data.cc` | string |  |
| `data.client_reference` | string |  |
| `data.from` | string |  |
| `data.is_delivered` | boolean |  |
| `data.is_hb` | boolean |  |
| `data.is_mailfailure` | boolean |  |
| `data.is_sb` | boolean |  |
| `data.mailagent_key` | string |  |
| `data.request_id` | string |  |
| `data.status` | string |  |
| `data.subject` | string |  |
| `data.to` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET email/email-reference/:emailReference` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-log.md) for the provider-specific parameters and requirements.

