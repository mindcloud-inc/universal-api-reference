# OneDesk: Search Customers With Details

Finds customers in OneDesk by filters, with details.

```
GET https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customers-with-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customers-with-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/search-customers-with-details?${params}`, {
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
| `properties[]` | array<object> | no | Array of OneDesk property filters. |
| `properties[].operation` | string | no | Comparison operation to apply to the property. |
| `properties[].property` | string | no | Name of property to be filtered. |
| `properties[].value` | string | no | Value used in the filter comparison. |
| `limit` | number | no | Maximum number of customer detail rows to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address1": {},
        "address2": {},
        "city": {},
        "country": {},
        "state": {},
        "zip": {}
      },
      "created": "2026-05-07T12:00:00.000Z",
      "customerOrganization": "string",
      "customerType": "string",
      "externalId": "string",
      "id": 1,
      "priority": 1,
      "profile": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "language": {},
        "lastName": "Chen",
        "phoneWork": {},
        "title": {}
      },
      "registered": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address1` | object |  |
| `address.address2` | object |  |
| `address.city` | object |  |
| `address.country` | object |  |
| `address.state` | object |  |
| `address.zip` | object |  |
| `created` | date |  |
| `customerOrganization` | string |  |
| `customerType` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `priority` | number |  |
| `profile.email` | string |  |
| `profile.firstName` | string |  |
| `profile.language` | object |  |
| `profile.lastName` | string |  |
| `profile.phoneWork` | object |  |
| `profile.title` | object |  |
| `registered` | boolean |  |

## Native endpoint

Through the native OneDesk API, this operation is `POST /rest/public/customers/filter/details` (base URL `https://app.onedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-customers-with-details.md) for the provider-specific parameters and requirements.

