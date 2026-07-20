# ServiceTrade: Update Quote

Updates an existing quote in ServiceTrade.

```
PUT https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/update-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/update-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "quoteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/update-quote', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "quoteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteId` | number | yes | Quote to update. |
| `notes` | string | no | Updated notes for the quote. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {
        "email": "ava@example.com",
        "id": 1
      },
      "contract": {
        "id": 1,
        "name": "Ava Chen"
      },
      "created": 1,
      "customer": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "customerPo": "string",
      "customerPoRequired": true,
      "externalIds": {
        "quickbooks": "string"
      },
      "id": 1,
      "items": [
        {
          "description": "string",
          "id": 1
        }
      ],
      "jobs": [
        {
          "id": 1,
          "name": "Ava Chen",
          "number": 1,
          "type": "string"
        }
      ],
      "jobType": "string",
      "latestAccepted": 1,
      "latestSubmission": 1,
      "location": {
        "address": {
          "city": "string",
          "state": "string"
        },
        "id": 1,
        "name": "Ava Chen",
        "refNumber": "string",
        "status": "string"
      },
      "name": "Ava Chen",
      "notes": "string",
      "owner": {
        "email": "ava@example.com",
        "id": 1
      },
      "quoteRequest": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string",
        "type": "string"
      },
      "refNumber": "string",
      "serviceLines": [
        {
          "abbr": "string",
          "id": 1,
          "name": "Ava Chen",
          "trade": "string"
        }
      ],
      "serviceRequests": [
        {
          "description": "string",
          "id": 1,
          "status": "string"
        }
      ],
      "status": "string",
      "subtotal": "string",
      "taxAmount": "string",
      "totalPrice": "string",
      "updated": 1,
      "uri": "string",
      "vendor": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo.email` | string |  |
| `assignedTo.id` | number |  |
| `contract.id` | number |  |
| `contract.name` | string |  |
| `created` | number |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customer.status` | string |  |
| `customerPo` | string |  |
| `customerPoRequired` | boolean |  |
| `externalIds.quickbooks` | string |  |
| `id` | number |  |
| `items[].description` | string |  |
| `items[].id` | number |  |
| `jobs[].id` | number |  |
| `jobs[].name` | string |  |
| `jobs[].number` | number |  |
| `jobs[].type` | string |  |
| `jobType` | string |  |
| `latestAccepted` | number |  |
| `latestSubmission` | number |  |
| `location.address.city` | string |  |
| `location.address.state` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `location.refNumber` | string |  |
| `location.status` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `owner.email` | string |  |
| `owner.id` | number |  |
| `quoteRequest.id` | number |  |
| `quoteRequest.name` | string |  |
| `quoteRequest.status` | string |  |
| `quoteRequest.type` | string |  |
| `refNumber` | string |  |
| `serviceLines[].abbr` | string |  |
| `serviceLines[].id` | number |  |
| `serviceLines[].name` | string |  |
| `serviceLines[].trade` | string |  |
| `serviceRequests[].description` | string |  |
| `serviceRequests[].id` | number |  |
| `serviceRequests[].status` | string |  |
| `status` | string |  |
| `subtotal` | string |  |
| `taxAmount` | string |  |
| `totalPrice` | string |  |
| `updated` | number |  |
| `uri` | string |  |
| `vendor.id` | number |  |
| `vendor.name` | string |  |
| `vendor.status` | string |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `PUT quote/:quoteId` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-quote.md) for the provider-specific parameters and requirements.

