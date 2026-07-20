# Zoho Mail: Mark Emails Unread

Marks emails as unread in Zoho Mail.

```
PUT https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/mark-emails-unread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/mark-emails-unread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/mark-emails-unread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | list<string> | yes | Zoho Mail account ID. |
| `messageId[]` | array<string> | no | One or more message IDs to mark as unread. Example: `11000000004001, 11000000004002`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId[]` | array<string> | no | One or more thread IDs to mark as unread instead of specific message IDs. Example: `11000000004001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "description": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Zoho Mail status code for the mark-as-unread request. |
| `description` | string | Zoho Mail status description for the mark-as-unread request. |

## Native endpoint

Through the native Zoho Mail API, this operation is `PUT /accounts/:accountId/updatemessage` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-emails-unread.md) for the provider-specific parameters and requirements.

