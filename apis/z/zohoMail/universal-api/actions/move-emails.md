# Zoho Mail: Move Emails

Moves emails to a folder in Zoho Mail.

```
PUT https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/move-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/move-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "destinationFolderId": "134143131"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/move-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "destinationFolderId": "134143131"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | list<string> | yes | Zoho Mail account ID. |
| `messageId[]` | array<string> | no | One or more message IDs to move. Example: `11000000004001`. |
| `destinationFolderId` | string | yes | Folder ID of the destination folder. Example: `134143131`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId[]` | array<string> | no | One or more thread IDs to move instead of specific message IDs. Example: `11000000004001`. |
| `isFolderSpecific` | boolean | no | Whether the move should be restricted to a specific source folder. |
| `folderId` | string | no | Source folder ID used when Folder Specific is true. Example: `12345`. |
| `isArchive` | boolean | no | Whether archived emails should also be included in the move action. |

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
| `code` | number | Zoho Mail status code for the move request. |
| `description` | string | Zoho Mail status description for the move request. |

## Native endpoint

Through the native Zoho Mail API, this operation is `PUT /accounts/:accountId/updatemessage` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-emails.md) for the provider-specific parameters and requirements.

