# Zoho CRM: Update Note

Updates an existing note in Zoho CRM.

```
PUT https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "noteId": "7323083000005207001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "noteId": "7323083000005207001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `noteId` | string | yes | Existing note ID. Example: `7323083000005207001`. |
| `data[].noteContent` | string | no | Updated note content. Example: `MindCloud action test note updated`. |
| `data[].noteTitle` | string | no | Updated note title. Example: `MindCloud test note updated`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[].isSharedToClient` | boolean | no | Updated client-sharing setting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Zoho result code. |
| `details` | object | Metadata about the updated note. |
| `message` | string | Zoho result message. |
| `status` | string | Zoho result status. |

## Native endpoint

Through the native Zoho CRM API, this operation is `PUT /Notes/:note_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

