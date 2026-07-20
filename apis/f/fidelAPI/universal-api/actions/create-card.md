# Fidel API: Create Card

Creates a card in a Fidel program.

```
POST https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "programId": "string",
  "countryCode": "string",
  "expMonth": 1,
  "expYear": 1,
  "number": "string",
  "termsOfUse": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "programId": "string",
    "countryCode": "string",
    "expMonth": 1,
    "expYear": 1,
    "number": "string",
    "termsOfUse": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `programId` | string | yes |  |
| `countryCode` | string | yes | Allowed values: CAN, DNK, FIN, GBR, IRL, JPN, NOR, SWE, USA. |
| `expMonth` | number | yes | The value must be between 1 and 12. |
| `expYear` | number | yes | 4 digits. CurrentYear <= ExpYear <= CurrentYear + 19. |
| `number` | string | yes | 15-16 long card number. |
| `termsOfUse` | boolean | yes | Cardholder accepted terms of use. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fidel API API returns.

## Native endpoint

Through the native Fidel API API, this operation is `POST /programs/:programId/cards` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card.md) for the provider-specific parameters and requirements.

