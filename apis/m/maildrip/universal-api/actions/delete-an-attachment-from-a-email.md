# Maildrip: Delete an attachment from a email



```
DELETE https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-an-attachment-from-a-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-an-attachment-from-a-email?connectionId=$CONNECTION_ID&emailId=ava%40example.com&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailId": "ava@example.com",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-an-attachment-from-a-email?${params}`, {
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
| `emailId` | string | yes | ID of the Email to delete attachment from |
| `attachmentId` | string | yes | ID of the attachment to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `DELETE /api/v1/attachments/` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-an-attachment-from-a-email.md) for the provider-specific parameters and requirements.

