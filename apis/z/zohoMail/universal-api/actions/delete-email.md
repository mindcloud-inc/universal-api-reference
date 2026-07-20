# Zoho Mail: Delete Email

Deletes an email from Zoho Mail.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/delete-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/delete-email?connectionId=$CONNECTION_ID&accountId=string&folderId=9000000002014&messageId=1710915488416100000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "folderId": "9000000002014",
  "messageId": "1710915488416100000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/delete-email?${params}`, {
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
| `accountId` | list<string> | yes | Zoho Mail account ID containing the email to delete. |
| `folderId` | string | yes | Folder ID containing the email to delete. Example: `9000000002014`. |
| `messageId` | string | yes | Message ID of the email to delete. Example: `1710915488416100000`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expunge` | boolean | no | Whether to permanently delete the email instead of moving it to Trash. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cId` | string | Delete confirmation identifier |

## Native endpoint

Through the native Zoho Mail API, this operation is `DELETE /accounts/:accountId/folders/:folderId/messages/:messageId` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-email.md) for the provider-specific parameters and requirements.

