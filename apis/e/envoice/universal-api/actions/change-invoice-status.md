# Envoice: Change Invoice Status

Updates an invoice status in Envoice.

```
PUT https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-invoice-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-invoice-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/change-invoice-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Invoice ID. |
| `status` | string | yes | Target invoice status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Success` | boolean | Whether Envoice changed the invoice status. |

## Native endpoint

Through the native Envoice API, this operation is `POST invoice/changestatus` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-invoice-status.md) for the provider-specific parameters and requirements.

