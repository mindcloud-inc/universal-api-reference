# Print.one Postcards: Get Batch Order

Retrieves a batch order from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-order?connectionId=$CONNECTION_ID&batchId=string&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string",
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/get-batch-order?${params}`, {
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
| `batchId` | string | yes | Batch ID to inspect |
| `orderId` | string | yes | Order ID to inspect |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "csvOrderId": "string",
      "errors": [
        "string"
      ],
      "finish": "string",
      "format": "string",
      "friendlyStatus": "string",
      "id": "string",
      "mergeVariables": {},
      "metadata": {},
      "recipient": {},
      "sendDate": "2026-05-07T12:00:00.000Z",
      "sender": {},
      "status": "string",
      "templateId": "string",
      "templateVersion": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string |  |
| `companyId` | string |  |
| `createdAt` | date |  |
| `csvOrderId` | string |  |
| `errors` | array<string> |  |
| `finish` | string |  |
| `format` | string |  |
| `friendlyStatus` | string |  |
| `id` | string |  |
| `mergeVariables` | object |  |
| `metadata` | object |  |
| `recipient` | object |  |
| `sendDate` | date |  |
| `sender` | object |  |
| `status` | string |  |
| `templateId` | string |  |
| `templateVersion` | number |  |
| `updatedAt` | date |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/batches/:batchId/orders/:orderId` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-order.md) for the provider-specific parameters and requirements.

