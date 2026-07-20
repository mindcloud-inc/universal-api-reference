# Billit: Create Party

Creates a new party in Billit.

```
POST https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-party
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-party" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Name": "Ava Chen",
  "PartyType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billit/latest/actions/create-party', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Name": "Ava Chen",
    "PartyType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Name` | string | yes | Company or contact display name. |
| `PartyType` | string | yes | Billit party type such as Customer or Supplier. |
| `VATNumber` | string | no | VAT number when available. |
| `Addresses[]` | array<object> | no | Billit address array. |
| `Identifiers[]` | array<object> | no | Optional alternate identifier array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | number | New Billit PartyID returned after party creation. |

## Native endpoint

Through the native Billit API, this operation is `POST /v1/parties` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-party.md) for the provider-specific parameters and requirements.

