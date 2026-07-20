# GatherUp: List Customers

Retrieves a list of customers from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/list-customers?${params}`, {
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
| `businessId` | number | no | Business ID (or multiple comma-separated ids.) |
| `customerId` | number | no | Customer ID |
| `customId` | string | no | Custom ID |
| `jobId` | string | no | Job ID |
| `email` | string | no | Customer email address. |
| `page` | number | no | Page. Default: `1`. |
| `subscription` | number | no | Subscription of customer. |
| `showHistory` | number | no | Show all related feedbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "count": 1,
      "createdAt": "string",
      "customId": "string",
      "email": "ava@example.com",
      "errorCode": 1,
      "errorMessage": "string",
      "firstName": "Ava",
      "id": 1,
      "jobId": "string",
      "lastName": "Chen",
      "page": 1,
      "pages": 1,
      "parentId": "string",
      "perPage": 1,
      "phone": "string",
      "rating": "string",
      "review": "string",
      "statusInfo": "string",
      "subscription": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `count` | number |  |
| `createdAt` | string |  |
| `customId` | string |  |
| `email` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `jobId` | string |  |
| `lastName` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `parentId` | string |  |
| `perPage` | number |  |
| `phone` | string |  |
| `rating` | string |  |
| `review` | string |  |
| `statusInfo` | string |  |
| `subscription` | number |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /customers/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

