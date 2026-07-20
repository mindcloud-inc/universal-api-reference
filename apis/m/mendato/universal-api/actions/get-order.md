# Mendato: Get Order



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-order?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-order?${params}`, {
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
| `variables` | object | yes | GraphQL variables object for the Mendato order query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": {
        "cancelledAt": "2026-05-07T12:00:00.000Z",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "endDate": "2026-05-07T12:00:00.000Z",
        "executionOnHolidays": true,
        "id": "string",
        "instructions": "string",
        "missingExecutors": 1,
        "number": 1,
        "requiredExecutors": 1,
        "startDate": "2026-05-07T12:00:00.000Z",
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
| `order.cancelledAt` | date |  |
| `order.createdAt` | date |  |
| `order.endDate` | date |  |
| `order.executionOnHolidays` | boolean |  |
| `order.id` | string |  |
| `order.instructions` | string |  |
| `order.missingExecutors` | number |  |
| `order.number` | number |  |
| `order.requiredExecutors` | number |  |
| `order.startDate` | date |  |
| `order.status` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

