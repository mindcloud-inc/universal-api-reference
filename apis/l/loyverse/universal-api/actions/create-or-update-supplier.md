# Loyverse: Create or Update Supplier

Creates or updates a supplier in Loyverse.

```
PUT https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-supplier', {
  method: 'PUT',
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
| `id` | string | no | The supplier id. If included in the POST request it will cause an update instead of a creating a new object. |
| `name` | string | yes | The supplier company name |
| `contact` | string | no | The supplier contact person name |
| `email` | string | no | The supplier email |
| `phoneNumber` | string | no |  |
| `website` | string | no | The supplier website page |
| `address1` | string | no | The supplier address |
| `address2` | string | no | The supplier address |
| `city` | string | no | The supplier city, town, or village. |
| `region` | string | no | The supplier’s region name. Typically a province, a state, or a prefecture. |
| `postalCode` | string | no | The supplier’s postal code, also known as zip, postcode, Eircode, etc. |
| `countryCode` | string | no | The two-letter country code corresponding to the supplier country in ISO 3166-1-alpha-2 format. |
| `note` | string | no |  |
| `createdAt` | date | no | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `updatedAt` | date | no | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `deletedAt` | date | no | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "city": "string",
      "contact": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "phoneNumber": "string",
      "postalCode": "string",
      "region": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string | The supplier address |
| `address2` | string | The supplier address |
| `city` | string | The supplier city, town, or village. |
| `contact` | string | The supplier contact person name |
| `countryCode` | string | The two-letter country code corresponding to the supplier country in ISO 3166-1-alpha-2 format. |
| `createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `email` | string | The supplier email |
| `id` | string | The supplier id. If included in the POST request it will cause an update instead of a creating a new object. |
| `name` | string | The supplier company name |
| `note` | string |  |
| `phoneNumber` | string |  |
| `postalCode` | string | The supplier’s postal code, also known as zip, postcode, Eircode, etc. |
| `region` | string | The supplier’s region name. Typically a province, a state, or a prefecture. |
| `updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `website` | string | The supplier website page |

## Native endpoint

Through the native Loyverse API, this operation is `POST /suppliers/` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-supplier.md) for the provider-specific parameters and requirements.

