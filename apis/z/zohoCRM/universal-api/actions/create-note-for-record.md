# Zoho CRM: Create Note for Record

Creates a new note for a Zoho CRM record.

```
POST https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-note-for-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-note-for-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[].parentRecord.id": "7323083000000731821",
  "data[].parentRecord.module.apiName": "Leads",
  "data[].noteContent": "MindCloud action test note"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/create-note-for-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[].parentRecord.id": "7323083000000731821",
    "data[].parentRecord.module.apiName": "Leads",
    "data[].noteContent": "MindCloud action test note"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[].parentRecord.id` | string | yes | Parent record ID for the note. Example: `7323083000000731821`. |
| `data[].parentRecord.module.apiName` | string | yes | Parent module API name for the note. Example: `Leads`. |
| `data[].noteContent` | string | yes | Body content for the note. Example: `MindCloud action test note`. |
| `data[].noteTitle` | string | no | Optional title for the note. Example: `MindCloud test note`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[].isSharedToClient` | boolean | no | Share the note to the client portal. |

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
| `details` | object | Metadata about the created note. |
| `message` | string | Zoho result message. |
| `status` | string | Zoho result status. |

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /Notes` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note-for-record.md) for the provider-specific parameters and requirements.

