# Retently: Get Customer

Retrieves a customer from Retently by ID.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-customer?${params}`, {
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
| `customerId` | string | yes | Customer Id |

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

Through the native Retently API, this operation is `GET /api/v2/customers/:customerId` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

