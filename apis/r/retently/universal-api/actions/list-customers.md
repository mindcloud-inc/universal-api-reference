# Retently: List Customers

Retrieves a list of customers from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&attributes%5B%5D.name=Ava%20Chen&attributes%5B%5D.op=string&attributes%5B%5D.value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "attributes[].name": "Ava Chen",
  "attributes[].op": "string",
  "attributes[].value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-customers?${params}`, {
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
| `email` | string | no | Find a customer by the email address; |
| `page` | number | no | The current page number. Default 1; Default: `1`. |
| `limit` | number | no | The items limit. Default 20. Maximum 1,000; Default: `20`. |
| `sort` | string | no | The sort option. Use '-' for DESC. Default '-createdDate'; |
| `startDate` | string | no | ISO format or UNIX timestamp; |
| `endDate` | string | no | ISO format or UNIX timestamp; |
| `attributes[]` | array<string> | no | Filter by customer properties. See Attributes Filtering section below; |
| `match` | string | no | Logic for multiple attribute filters. Values: 'all' (AND, default), 'any' (OR); Default: `all`. |
| `attributes[].name` | string | yes | Attribute field name |
| `attributes[].op` | string | yes | Filter operator |
| `attributes[].value` | string | yes | Attribute match value |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdDate": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "integrationsLists": [
        "string"
      ],
      "isAnonymous": true,
      "isAtRisk": true,
      "isEmailDeliverable": true,
      "isInQueue": true,
      "isInQueueSetAt": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "lastSurveySent": {},
      "location": {},
      "phoneNumber": "string",
      "properties": [
        {}
      ],
      "source": "string",
      "surveySubscriptionStatus": {},
      "syncId": "string",
      "tags": [
        "string"
      ],
      "updatedDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdDate` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `integrationsLists` | array<string> |  |
| `isAnonymous` | boolean |  |
| `isAtRisk` | boolean |  |
| `isEmailDeliverable` | boolean |  |
| `isInQueue` | boolean |  |
| `isInQueueSetAt` | string |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `lastSurveySent` | object |  |
| `location` | object |  |
| `phoneNumber` | string |  |
| `properties` | array<object> |  |
| `source` | string |  |
| `surveySubscriptionStatus` | object |  |
| `syncId` | string |  |
| `tags` | array<string> |  |
| `updatedDate` | string |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/customers` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

