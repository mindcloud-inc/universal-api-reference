# Shipcloud: List Addresses

Retrieves addresses from Shipcloud.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-addresses?${params}`, {
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
| `careOf` | string | no | Filter addresses by care-of value. |
| `city` | string | no | Filter addresses by city. |
| `company` | string | no | Filter addresses by company name. |
| `country` | string | no | Filter addresses by ISO country code. |
| `firstName` | string | no | Filter addresses by first name. |
| `lastName` | string | no | Filter addresses by last name. |
| `page` | number | no | Page number for paginated address results. |
| `perPage` | number | no | Number of address records to return per page. |
| `phone` | string | no | Filter addresses by phone number. |
| `street` | string | no | Filter addresses by street name. |
| `streetNo` | string | no | Filter addresses by street number. |
| `zipCode` | string | no | Filter addresses by ZIP or postal code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "care_of": "string",
      "city": "string",
      "company": "string",
      "country": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "phone": "string",
      "state": "string",
      "street": "string",
      "street_no": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `care_of` | string |  |
| `city` | string |  |
| `company` | string |  |
| `country` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `street` | string |  |
| `street_no` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /addresses` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-addresses.md) for the provider-specific parameters and requirements.

