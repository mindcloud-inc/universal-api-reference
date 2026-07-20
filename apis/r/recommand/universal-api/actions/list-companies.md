# Recommand: List Companies

Retrieves company records from the Recommand API.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-companies?${params}`, {
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
| `enterprisenumber` | string | no | enterpriseNumber parameter. |
| `vatnumber` | string | no | vatNumber parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        {
          "address": "string",
          "city": "string",
          "country": "string",
          "createdAt": "string",
          "email": "ava@example.com",
          "enterpriseNumber": "string",
          "enterpriseNumberScheme": "string",
          "id": "string",
          "isSmpRecipient": true,
          "isVerified": true,
          "name": "Ava Chen",
          "phone": "string",
          "postalCode": "string",
          "teamId": "string",
          "updatedAt": "string",
          "vatNumber": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies` | array<object> |  |
| `companies[].address` | string |  |
| `companies[].city` | string |  |
| `companies[].country` | string |  |
| `companies[].createdAt` | string |  |
| `companies[].email` | string |  |
| `companies[].enterpriseNumber` | string |  |
| `companies[].enterpriseNumberScheme` | string |  |
| `companies[].id` | string |  |
| `companies[].isSmpRecipient` | boolean |  |
| `companies[].isVerified` | boolean |  |
| `companies[].name` | string |  |
| `companies[].phone` | string |  |
| `companies[].postalCode` | string |  |
| `companies[].teamId` | string |  |
| `companies[].updatedAt` | string |  |
| `companies[].vatNumber` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/companies` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

