# ReputationLync: List Customers

Retrieves customers from ReputationLync.

```
GET https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReputationLync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reputationLync/latest/actions/list-customers?${params}`, {
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
| `customerId` | string | no | Return a specific customer by ReputationLync customer ID. Example: `824925`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | string | no | Filter customers by location identifier. Example: `12345`. |
| `createdAfterDate` | string | no | Only return customers created after this date. Example: `2023-04-01 00:00:00`. |
| `createdBeforeDate` | string | no | Only return customers created before this date. Example: `2023-04-30 23:59:59`. |
| `createdAfterId` | string | no | Only return customers created after this internal record ID. Example: `824000`. |
| `createdBeforeId` | string | no | Only return customers created before this internal record ID. Example: `825000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logId": 1,
      "result": [
        {}
      ],
      "resultCount": 1,
      "status": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logId` | number | Provider log identifier for the request. |
| `result` | array<object> | Matched customer records returned by ReputationLync. |
| `resultCount` | number | Number of matched customer records returned in the result array. |
| `status` | string | Provider status for the list-customer request. |
| `userId` | string | ReputationLync user identifier associated with the request. |

## Native endpoint

Through the native ReputationLync API, this operation is `POST /listCustomer` (base URL `https://reputationlync.com/app/api/customer`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

