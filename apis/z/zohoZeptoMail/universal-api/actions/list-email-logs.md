# Zoho ZeptoMail: List Email Logs

Retrieves email logs from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-email-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-email-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/list-email-logs?${params}`, {
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
| `bcc` | string | no | BCC recipient address to filter by. |
| `cc` | string | no | CC recipient address to filter by. |
| `clientReference` | string | no | Client reference identifier to filter by. |
| `dateFrom` | string | no | Start of the log search window. |
| `dateTo` | string | no | End of the log search window. |
| `from` | string | no | Sender address to filter by. |
| `isDelivered` | boolean | no | Filter for delivered email logs. |
| `isHb` | boolean | no | Filter for hard bounced email logs. |
| `isMailfailure` | boolean | no | Filter for processed failed email logs. |
| `isSb` | boolean | no | Filter for soft bounced email logs. |
| `limit` | number | no | Maximum number of log records to return. |
| `mailAgentKey` | string | no | Agent alias to filter email logs. |
| `offset` | number | no | Number of log records to skip. |
| `recipient` | string | no | Recipient address across delivery fields. |
| `requestId` | string | no | Request identifier of the email. |
| `subject` | string | no | Email subject to filter by. |
| `to` | string | no | Recipient address to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].bcc` | string |  |
| `data[].cc` | string |  |
| `data[].client_reference` | string |  |
| `data[].from` | string |  |
| `data[].is_delivered` | boolean |  |
| `data[].is_hb` | boolean |  |
| `data[].is_mailfailure` | boolean |  |
| `data[].is_sb` | boolean |  |
| `data[].mailagent_key` | string |  |
| `data[].request_id` | string |  |
| `data[].status` | string |  |
| `data[].subject` | string |  |
| `data[].to` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET email` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-logs.md) for the provider-specific parameters and requirements.

