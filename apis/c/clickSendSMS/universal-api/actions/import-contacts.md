# ClickSend SMS: Import Contacts

Imports contacts into a ClickSend SMS list.

```
POST https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/import-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/import-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": 1,
  "fileUrl": "https://example.com",
  "field_order[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/import-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": 1,
    "fileUrl": "https://example.com",
    "field_order[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_id` | number | yes | List identifier. |
| `fileUrl` | string | yes | Public URL to CSV/XLS/XLSX import file. |
| `field_order[]` | array<string> | yes | Ordered list of contact field names in the file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": 1,
      "httpCode": 1,
      "responseCode": "string",
      "responseMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | number |  |
| `httpCode` | number |  |
| `responseCode` | string |  |
| `responseMsg` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `POST /v3/lists/:list_id/import` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts.md) for the provider-specific parameters and requirements.

