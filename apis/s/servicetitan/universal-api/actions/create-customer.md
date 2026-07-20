# ServiceTitan: Create Customer

Creates a new customer in ServiceTitan.

```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address.street": "string",
  "locations[].address.street": "string",
  "locations[].name": "Ava Chen",
  "name": "Ava Chen",
  "locations[].address": {},
  "locations[].contacts[].value": "string",
  "address.city": "string",
  "locations[].address.city": "string",
  "locations[].contacts[].type": "string",
  "address.state": "string",
  "locations[].address.zip": "string",
  "address.zip": "string",
  "locations[]": [
    {}
  ],
  "locations[].address.state": "string",
  "address": {},
  "address.country": "string",
  "locations[].address.country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address.street": "string",
    "locations[].address.street": "string",
    "locations[].name": "Ava Chen",
    "name": "Ava Chen",
    "locations[].address": {},
    "locations[].contacts[].value": "string",
    "address.city": "string",
    "locations[].address.city": "string",
    "locations[].contacts[].type": "string",
    "address.state": "string",
    "locations[].address.zip": "string",
    "address.zip": "string",
    "locations[]": [{}],
    "locations[].address.state": "string",
    "address": {},
    "address.country": "string",
    "locations[].address.country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memo` | string | no |  |
| `address.street` | string | yes |  |
| `contacts[].value` | string | no |  |
| `customFields[].typeId` | number | no |  |
| `externalData.externalData[].value` | string | no |  |
| `locations[].address.street` | string | yes |  |
| `locations[].contacts[].memo` | string | no |  |
| `locations[].externalData.externalData[].value` | string | no |  |
| `locations[].name` | string | yes |  |
| `name` | string | yes |  |
| `address.unit` | string | no |  |
| `contacts[].type` | list<string> | no |  |
| `customFields[].value` | string | no |  |
| `externalData.applicationGuid` | string | no |  |
| `externalData.externalData[].key` | string | no |  |
| `locations[].address` | object | yes |  |
| `locations[].address.unit` | string | no |  |
| `locations[].contacts[].value` | string | yes |  |
| `locations[].externalData.applicationGuid` | string | no |  |
| `locations[].externalData.externalData[].key` | string | no |  |
| `address.city` | string | yes |  |
| `contacts[].type` | list<string> | no |  |
| `customFields[].name` | string | no | Name/label of the custom field |
| `doNotMail` | boolean | no | Default: `false`. |
| `externalData.externalData[]` | array | no |  |
| `locations[].address.city` | string | yes |  |
| `locations[].contacts[]` | array<object> | no |  |
| `locations[].contacts[].type` | string<string> | yes |  |
| `locations[].externalData.externalData[]` | array | no |  |
| `address.state` | string | yes |  |
| `doNotService` | boolean | no | Default: `false`. |
| `locations[].address.zip` | string | yes |  |
| `locations[].tagTypeIds[]` | array<number> | no |  |
| `address.zip` | string | yes |  |
| `locations[]` | array<object> | yes | Locations for the customer |
| `locations[].address.state` | string | yes |  |
| `locations[].externalData` | object | no |  |
| `address` | object<object> | yes | Bill-To address of the customer record |
| `address.country` | string | yes |  |
| `externalData` | object | no |  |
| `locations[].address.country` | string | yes |  |
| `address.longitude` | number | no |  |
| `contacts[]` | array<object> | no |  |
| `locations[].latitude` | number | no |  |
| `address.latitude` | number | no |  |
| `customFields[]` | array<object> | no |  |
| `locations[].longitude` | number | no |  |
| `tagTypeIds[]` | array<number> | no |  |
| `type` | string | no | Residential or commercial |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST crm/v2/tenant/{{credentials.tenant}}/customers` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

