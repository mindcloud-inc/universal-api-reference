# Wati: Send Template Messages CSV

Sends template messages from a CSV file in Wati.

```
POST https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-messages-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-messages-csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateName": "Ava Chen",
  "broadcastName": "Ava Chen",
  "whatsapp_numbers_csv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wati/latest/actions/send-template-messages-csv', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateName": "Ava Chen",
    "broadcastName": "Ava Chen",
    "whatsapp_numbers_csv": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateName` | string | yes | Approved Wati template name. |
| `broadcastName` | string | yes | Name for the broadcast record. |
| `whatsapp_numbers_csv` | file | yes | CSV file containing recipient phone numbers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | string | Provider message about the uploaded recipient file. |
| `result` | boolean | Whether Wati accepted the CSV broadcast request. |

## Native endpoint

Through the native Wati API, this operation is `POST /api/v1/sendTemplateMessageCSV` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-template-messages-csv.md) for the provider-specific parameters and requirements.

