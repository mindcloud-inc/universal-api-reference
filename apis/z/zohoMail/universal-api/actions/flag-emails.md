# Zoho Mail: Flag Emails

Flags email messages in Zoho Mail.

```
PUT https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/flag-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/flag-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "flagId": "flag_not_set"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/flag-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "flagId": "flag_not_set"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | list<string> | yes | Zoho Mail account ID. |
| `messageId[]` | array<string> | no | One or more message IDs to flag. Example: `123456780, 987654321`. |
| `flagId` | list<string> | yes | Flag to apply to the selected emails. One of: `flag_not_set`, `followup`, `important`, `info`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId[]` | array<string> | no | One or more thread IDs to flag instead of specific message IDs. Example: `123456780`. |
| `isFolderSpecific` | boolean | no | Whether the flag update should be restricted to a specific folder. |
| `folderId` | string | no | Folder ID used when Folder Specific is true. Example: `12345`. |
| `isArchive` | boolean | no | Whether archived emails should also be included in the flag action. |

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
| `code` | number | Zoho Mail status code for the flag update request. |
| `description` | string | Zoho Mail status description for the flag update request. |

## Native endpoint

Through the native Zoho Mail API, this operation is `PUT /accounts/:accountId/updatemessage` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/flag-emails.md) for the provider-specific parameters and requirements.

