# Teamhood: Get Attachment

Retrieves attachment metadata from Teamhood by ID.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/get-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/get-attachment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/get-attachment?${params}`, {
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
| `id` | string | no | The Teamhood attachment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "itemId": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The Teamhood attachment ID. |
| `itemId` | string | The Teamhood item ID that owns the attachment. |
| `mimeType` | string | The attachment MIME type. |
| `name` | string | The attachment file name. |
| `size` | number | The attachment size in bytes. |

## Native endpoint

Through the native Teamhood API, this operation is `GET /attachments/:id` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment.md) for the provider-specific parameters and requirements.

