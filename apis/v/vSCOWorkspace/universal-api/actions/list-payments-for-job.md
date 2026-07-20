# VSCO Workspace: List Payments for Job

Retrieves payments for a job in VSCO Workspace.

```
GET https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-payments-for-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-payments-for-job?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-payments-for-job?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "authCode": "string",
      "checkNumber": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "hidden": true,
      "id": "string",
      "invoiceItemId": "string",
      "jobId": "string",
      "memo": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "payerId": "string",
      "paymentAllocations": [
        {}
      ],
      "paymentMethodId": "string",
      "processedViaClientAccess": true,
      "received": "2026-05-07T12:00:00.000Z",
      "refundedAmount": {},
      "refunds": [
        {}
      ],
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `authCode` | string |  |
| `checkNumber` | string |  |
| `created` | date | A server timestamp (always in UTC) |
| `hidden` | boolean | Whether or not the object is hidden. |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `invoiceItemId` | string | A ULID entity identifier that is nullable. |
| `jobId` | string | A ULID entity identifier that is nullable. |
| `memo` | string |  |
| `modified` | date | A server timestamp (always in UTC) |
| `payerId` | string | A ULID entity identifier that is nullable. |
| `paymentAllocations` | array<object> |  |
| `paymentMethodId` | string | A ULID entity identifier that is nullable. |
| `processedViaClientAccess` | boolean |  |
| `received` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `refundedAmount` | object |  |
| `refunds` | array<object> |  |
| `status` | string |  |
| `transactionId` | string |  |

## Native endpoint

Through the native VSCO Workspace API, this operation is `GET /job/:id/payment` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments-for-job.md) for the provider-specific parameters and requirements.

