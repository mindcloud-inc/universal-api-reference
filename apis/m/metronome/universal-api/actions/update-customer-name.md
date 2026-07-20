# Metronome: Update Customer Name

Updates a customer name in Metronome.

```
PUT https://connect.mindcloud.co/v1/universal/metronome/latest/actions/update-customer-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/update-customer-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metronome/latest/actions/update-customer-name', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The customer ID. |
| `name` | string | yes | The new customer name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_id": "string",
      "id": "string",
      "ingest_aliases": [
        "string"
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_id` | string |  |
| `id` | string |  |
| `ingest_aliases[]` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/customers/:customer_id/setName` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-name.md) for the provider-specific parameters and requirements.

