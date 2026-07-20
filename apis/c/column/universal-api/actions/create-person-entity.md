# Column: Create Person Entity



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/create-person-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/create-person-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "ssn": "string",
  "dateOfBirth": "string",
  "address.line1": "string",
  "address.city": "string",
  "address.state": "string",
  "address.postalCode": "string",
  "address.countryCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/create-person-entity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "ssn": "string",
    "dateOfBirth": "string",
    "address.line1": "string",
    "address.city": "string",
    "address.state": "string",
    "address.postalCode": "string",
    "address.countryCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | First name of the individual. |
| `lastName` | string | yes | Last name of the individual. |
| `ssn` | string | yes | Social Security Number. |
| `dateOfBirth` | string | yes | Date of birth in YYYY-MM-DD format. |
| `address.line1` | string | yes | Street address line 1. |
| `address.city` | string | yes | City. |
| `address.state` | string | yes | State or province. |
| `address.postalCode` | string | yes | Postal code. |
| `address.countryCode` | string | yes | ISO 3166-1 Alpha-2 country code. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `POST /entities/person` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person-entity.md) for the provider-specific parameters and requirements.

