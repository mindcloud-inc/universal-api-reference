# ServiceTrade: Get Contact by ID

Retrieves a contact from ServiceTrade by ID.

```
GET https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-contact-by-id?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/get-contact-by-id?${params}`, {
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
| `contactId` | number | yes | ID of the contact to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternatePhone": "string",
      "company": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "created": 1,
      "email": "ava@example.com",
      "externalIds": {
        "quickbooks": "string"
      },
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "location": {
        "address": {
          "city": "string",
          "postalCode": "string",
          "state": "string",
          "street": "string"
        },
        "id": 1,
        "name": "Ava Chen",
        "refNumber": "string",
        "status": "string"
      },
      "mobile": "string",
      "phone": "string",
      "status": "string",
      "type": "string",
      "types": [
        "string"
      ],
      "updated": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternatePhone` | string |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `company.status` | string |  |
| `created` | number |  |
| `email` | string |  |
| `externalIds.quickbooks` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `location.address.city` | string |  |
| `location.address.postalCode` | string |  |
| `location.address.state` | string |  |
| `location.address.street` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `location.refNumber` | string |  |
| `location.status` | string |  |
| `mobile` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `type` | string |  |
| `types[]` | string |  |
| `updated` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `GET contact/:contactId` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-id.md) for the provider-specific parameters and requirements.

