# ServiceTitan: Update Costumer

Updates an existing customer in ServiceTitan.

```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-costumer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-costumer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-costumer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memo` | string | no |  |
| `address.street` | string | no |  |
| `contacts[].value` | string | no |  |
| `customFields[].typeId` | number | no |  |
| `locations[].address.street` | string | no |  |
| `locations[].contacts[].memo` | string | no |  |
| `locations[].externalData.externalData[].value` | string | no |  |
| `locations[].name` | string | no |  |
| `name` | string | no |  |
| `address.unit` | string | no |  |
| `contacts[].type` | list<string> | no |  |
| `customFields[].value` | string | no |  |
| `locations[].address` | object | no |  |
| `locations[].address.unit` | string | no |  |
| `locations[].contacts[].value` | string | no |  |
| `locations[].externalData.applicationGuid` | string | no |  |
| `locations[].externalData.externalData[].key` | string | no |  |
| `address.city` | string | no |  |
| `contacts[].type` | list<string> | no |  |
| `customFields[].name` | string | no | Name/label of the custom field |
| `doNotMail` | boolean | no | Default: `false`. |
| `locations[].address.city` | string | no |  |
| `locations[].contacts[]` | array<object> | no |  |
| `locations[].contacts[].type` | string<string> | no |  |
| `locations[].externalData.externalData[]` | array | no |  |
| `address.state` | string | no |  |
| `doNotService` | boolean | no | Default: `false`. |
| `locations[].address.zip` | string | no |  |
| `locations[].tagTypeIds[]` | array<number> | no |  |
| `address.zip` | string | no |  |
| `locations[]` | array<object> | no | Locations for the customer |
| `locations[].address.state` | string | no |  |
| `locations[].externalData` | object | no |  |
| `address` | object<object> | no | Bill-To address of the customer record |
| `address.country` | string | no |  |
| `externalData` | object | no |  |
| `locations[].address.country` | string | no |  |
| `address.longitude` | number | no |  |
| `contacts[]` | array<object> | no |  |
| `locations[].latitude` | number | no |  |
| `address.latitude` | number | no |  |
| `customFields[]` | array<object> | no |  |
| `locations[].longitude` | number | no |  |
| `tagTypeIds[]` | array<number> | no |  |
| `type` | string | no | Residential or commercial |
| `customerId` | string | yes |  |
| `customFields` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH crm/v2/tenant/{{credentials.tenant}}/customers/:customerId` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/update-costumer.md) for the provider-specific parameters and requirements.

