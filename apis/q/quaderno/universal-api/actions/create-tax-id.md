# Quaderno: Create Tax ID

Creates a registered tax ID in Quaderno.

```
POST https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-tax-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-tax-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jurisdictionId": "11",
  "value": "FR40303265045"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-tax-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jurisdictionId": "11",
    "value": "FR40303265045"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jurisdictionId` | number | yes | Jurisdiction ID to register. Example: `11`. |
| `value` | string | yes | Tax ID value. Example: `FR40303265045`. |
| `validFrom` | date | no | Start date for validity. Example: `2026-03-21`. |
| `validUntil` | date | no | End date for validity. Example: `2026-12-31`. |
| `permanentEstablishment` | boolean | no | Whether this is a permanent establishment. Example: `false`. |
| `importScheme` | boolean | no | Whether the registration uses the import scheme. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": 1,
      "importScheme": true,
      "jurisdiction": {
        "country": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "permanentEstablishment": true,
      "state": "string",
      "validFrom": "string",
      "validUntil": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `id` | number |  |
| `importScheme` | boolean |  |
| `jurisdiction.country` | string |  |
| `jurisdiction.id` | number |  |
| `jurisdiction.name` | string |  |
| `permanentEstablishment` | boolean |  |
| `state` | string |  |
| `validFrom` | string |  |
| `validUntil` | object |  |
| `value` | string |  |

## Native endpoint

Through the native Quaderno API, this operation is `POST /tax_ids` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tax-id.md) for the provider-specific parameters and requirements.

