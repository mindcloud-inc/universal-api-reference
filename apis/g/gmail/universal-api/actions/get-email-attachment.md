# Google Mail: Get Email Attachment

Retrieves a Gmail message attachment.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email-attachment?connectionId=$CONNECTION_ID&messageId=17c7f5f9f1d6c1a2&id=ANGjdJ9A..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "17c7f5f9f1d6c1a2",
  "id": "ANGjdJ9A..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email-attachment?${params}`, {
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
| `messageId` | string | yes | The Gmail message ID that contains the attachment. Example: `17c7f5f9f1d6c1a2`. |
| `id` | string | yes | Attachment ID from the message payload. Example: `ANGjdJ9A...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /messages/:messageId/attachments/:id` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-attachment.md) for the provider-specific parameters and requirements.

