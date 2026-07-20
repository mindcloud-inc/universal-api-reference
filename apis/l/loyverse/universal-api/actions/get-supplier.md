# Loyverse: Get Supplier

Retrieves a supplier record from Loyverse.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-supplier?connectionId=$CONNECTION_ID&supplierId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supplierId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-supplier?${params}`, {
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
| `supplierId` | string | yes |  |

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

Through the native Loyverse API, this operation is `GET /suppliers/:supplier_id` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier.md) for the provider-specific parameters and requirements.

