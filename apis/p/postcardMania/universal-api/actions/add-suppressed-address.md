# PostcardMania: Add Suppressed Address

Creates a new suppressed address in PostcardMania.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/add-suppressed-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/add-suppressed-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string",
  "city": "string",
  "state": "string",
  "zipCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/add-suppressed-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string",
    "city": "string",
    "state": "string",
    "zipCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | Street address to suppress. |
| `city` | string | yes | City for the suppressed address. |
| `state` | string | yes | State or province for the suppressed address. |
| `zipCode` | string | yes | Postal code for the suppressed address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "suppressionAddressID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `suppressionAddressID` | number | Identifier for the newly created suppressed address entry. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /suppression-list` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-suppressed-address.md) for the provider-specific parameters and requirements.

