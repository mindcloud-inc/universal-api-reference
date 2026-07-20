# Dukaan: Update Customer Notes

Updates customer notes in Dukaan.

```
PUT https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/update-customer-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/update-customer-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storeLeadId": "21881957",
  "notes": "Added a customer note"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/update-customer-notes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storeLeadId": "21881957",
    "notes": "Added a customer note"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storeLeadId` | number | yes | Dukaan store lead/customer ID. Example: `21881957`. |
| `notes` | string | yes | Customer note text. Example: `Added a customer note`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Dukaan customer record ID |
| `modified_at` | date | Last modified timestamp |
| `notes` | string | Updated customer notes |
| `uuid` | string | Dukaan customer UUID |

## Native endpoint

Through the native Dukaan API, this operation is `PATCH api/order/seller/:storeLeadId/update-storelead-notes/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-notes.md) for the provider-specific parameters and requirements.

