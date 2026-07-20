# Metronome: Create Customer

Creates a new customer in Metronome.

```
POST https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/metronome/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The customer name. |
| `ingestAliases[]` | array<string> | no | Aliases that can identify the customer in usage events. Accepts multiple values as an array. |
| `externalId` | string | no | Deprecated alias that can identify the customer in usage events. |

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

Through the native Metronome API, this operation is `POST /v1/customers` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

