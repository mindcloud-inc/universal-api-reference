# Synchroteam: Send Invoice or Quotation

Creates or updates an invoice or quotation in Synchroteam.

```
PUT https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/send-invoice-or-quotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/send-invoice-or-quotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/send-invoice-or-quotation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes | Request body payload for creating or updating an invoice (per docs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "num": 1,
        "numberLines": 1
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.num` | number |  |
| `data.numberLines` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `POST /Api/v2/Invoices/Send` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-invoice-or-quotation.md) for the provider-specific parameters and requirements.

