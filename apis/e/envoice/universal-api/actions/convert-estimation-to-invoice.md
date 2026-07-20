# Envoice: Convert Estimation to Invoice

Converts an estimation to an invoice in Envoice.

```
POST https://connect.mindcloud.co/v1/universal/envoice/latest/actions/convert-estimation-to-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/convert-estimation-to-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoice/latest/actions/convert-estimation-to-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Estimation identifier to convert to an invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Client": {},
      "Id": 1,
      "Items": [
        {}
      ],
      "Number": "string",
      "Status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Client` | object | Invoice client. |
| `Id` | number | Created invoice identifier. |
| `Items` | array<object> | Invoice line items. |
| `Number` | string | Invoice number. |
| `Status` | number | Invoice status. |

## Native endpoint

Through the native Envoice API, this operation is `POST estimation/convert` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-estimation-to-invoice.md) for the provider-specific parameters and requirements.

