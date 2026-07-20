# Loyverse: List Suppliers

Retrieves supplier records from the Loyverse account.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-suppliers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `suppliersIds` | string | no | Return only suppliers specified by a comma-separated list of IDs |
| `limit` | number | no | Used for pagination |
| `cursor` | string | no | Used for pagination |
| `showDeleted` | boolean | no | Show deleted modifiers and modifier options |

## Response

```json
{
  "success": true,
  "data": [
    {
      "suppliers": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `suppliers` | array<object> |  |
| `suppliers[].address1` | string | The supplier address |
| `suppliers[].address2` | string | The supplier address |
| `suppliers[].city` | string | The supplier city, town, or village. |
| `suppliers[].contact` | string | The supplier contact person name |
| `suppliers[].countryCode` | string | The two-letter country code corresponding to the supplier country in ISO 3166-1-alpha-2 format. |
| `suppliers[].createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `suppliers[].deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `suppliers[].email` | string | The supplier email |
| `suppliers[].id` | string | The supplier id. If included in the POST request it will cause an update instead of a creating a new object. |
| `suppliers[].name` | string | The supplier company name |
| `suppliers[].note` | string |  |
| `suppliers[].phoneNumber` | string |  |
| `suppliers[].postalCode` | string | The supplier’s postal code, also known as zip, postcode, Eircode, etc. |
| `suppliers[].region` | string | The supplier’s region name. Typically a province, a state, or a prefecture. |
| `suppliers[].updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `suppliers[].website` | string | The supplier website page |

## Native endpoint

Through the native Loyverse API, this operation is `GET /suppliers/` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

