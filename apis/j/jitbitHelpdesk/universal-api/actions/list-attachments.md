# Jitbit Helpdesk: List Attachments



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-attachments?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-attachments?${params}`, {
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
| `id` | number | yes | Jitbit ticket ID to list attachments for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileId": 1,
      "fileName": "Ava Chen",
      "fileSize": 1,
      "issueId": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileId` | number | Attachment file ID. |
| `fileName` | string | Attachment file name. |
| `fileSize` | number | Attachment file size in bytes. |
| `issueId` | number | Parent ticket ID. |
| `url` | string | Attachment download URL. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /Attachments` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attachments.md) for the provider-specific parameters and requirements.

