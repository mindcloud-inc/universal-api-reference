# Housecall Pro: List Customers



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-customers?${params}`, {
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
| `q` | string | no | Search customers by name, email, mobile number, or address. Example: `apps@mindcloud.co`. |
| `locationIds[]` | array<string> | no | IDs of locations to pull customers from. Accepts multiple values as an array. Example: `loc_123,loc_456`. |
| `expand[]` | array<string> | no | Fields to expand in the response body. Accepts multiple values as an array. Example: `attachments`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "company": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "homeNumber": "string",
      "id": "string",
      "lastName": "Chen",
      "leadSource": "string",
      "mobileNumber": "string",
      "notes": "string",
      "notificationsEnabled": true,
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `company` | string |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `homeNumber` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `leadSource` | string |  |
| `mobileNumber` | string |  |
| `notes` | string |  |
| `notificationsEnabled` | boolean |  |
| `tags` | array<string> |  |
| `updatedAt` | string |  |
| `workNumber` | string |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /customers` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

