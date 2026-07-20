# Parsio: Update Mailbox



```
PUT https://connect.mindcloud.co/v1/universal/parsio/latest/actions/update-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/update-mailbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailboxId": "string",
  "emailPrefix": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parsio/latest/actions/update-mailbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailboxId": "string",
    "emailPrefix": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailboxId` | string | yes | Parsio mailbox ID. |
| `name` | string | no | Mailbox name. |
| `emailPrefix` | string | yes | Mailbox email prefix. |
| `processAttachments` | boolean | no | Whether to store email attachments. |
| `collectEmails` | boolean | no | Whether to collect email addresses automatically. |
| `alertEmailHours` | number | no | Email alert frequency in hours. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errFields": {},
      "errMsg": "string",
      "isError": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errFields` | object | Provider error field details. |
| `errMsg` | string | Provider error message. |
| `isError` | boolean | Whether the update failed. |

## Native endpoint

Through the native Parsio API, this operation is `POST /mailboxes/:mailbox_id` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mailbox.md) for the provider-specific parameters and requirements.

