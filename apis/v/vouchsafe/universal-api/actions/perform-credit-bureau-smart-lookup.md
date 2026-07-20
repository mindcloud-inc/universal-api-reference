# Vouchsafe: Perform Credit Bureau Smart Lookup

Runs a credit bureau smart lookup in Vouchsafe.

```
POST https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-credit-bureau-smart-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchsafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-credit-bureau-smart-lookup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "firstLineOfAddress": "string",
  "postcode": "string",
  "dateOfBirth": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/perform-credit-bureau-smart-lookup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "firstLineOfAddress": "string",
    "postcode": "string",
    "dateOfBirth": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Given name(s). |
| `lastName` | string | yes | Family name. |
| `firstLineOfAddress` | string | yes | First line of address taken from the postcode lookup results. |
| `postcode` | string | yes | Postcode used in the postcode lookup. |
| `dateOfBirth` | string | yes | Date of birth in YYYY-MM-DD or ISO 8601 format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchsafe API returns.

## Native endpoint

Through the native Vouchsafe API, this operation is `POST /smart-lookups` (base URL `https://app.vouchsafe.id/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-credit-bureau-smart-lookup.md) for the provider-specific parameters and requirements.

