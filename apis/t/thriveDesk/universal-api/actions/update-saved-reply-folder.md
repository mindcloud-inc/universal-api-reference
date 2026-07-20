# ThriveDesk: Update Saved Reply Folder



```
PUT https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/update-saved-reply-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/update-saved-reply-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/update-saved-reply-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "data": {},
      "folder_id": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Saved reply content when returned. |
| `data` | object | Raw saved reply payload. |
| `folder_id` | string | Saved reply folder identifier when returned. |
| `id` | string | Saved reply identifier. |
| `name` | string | Saved reply name when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `PATCH /v1/saved-replies/folder` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-saved-reply-folder.md) for the provider-specific parameters and requirements.

