# Billit: Update Party

Updates an existing party in Billit.

```
PUT https://connect.mindcloud.co/v1/universal/billit/latest/actions/update-party
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/billit/latest/actions/update-party" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "partyID": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billit/latest/actions/update-party', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "partyID": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partyID` | number | yes | Billit PartyID. |
| `Name` | string | no | Updated display name. |
| `VATNumber` | string | no | Updated VAT number. |
| `Addresses[]` | array<object> | no | Updated addresses array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Billit patch response payload. |

## Native endpoint

Through the native Billit API, this operation is `PATCH /v1/parties/:partyID` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-party.md) for the provider-specific parameters and requirements.

