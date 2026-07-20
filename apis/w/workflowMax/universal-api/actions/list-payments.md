# WorkflowMax: List Payments



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-payments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "amount": 1,
          "createdAt": "string",
          "date": "string",
          "invoiceUUID": "string",
          "reference": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].amount` | number | The amount of the payment. |
| `data[].createdAt` | string | The UTC timestamp indicating when the payment was created. |
| `data[].date` | string | The date of the payment. |
| `data[].invoiceUUID` | string | The unique identifier of the invoice associated with the payment. |
| `data[].reference` | string | The reference of the payment. |
| `data[].updatedAt` | string | The UTC timestamp indicating when the payment was last updated. |
| `data[].uuid` | string | The unique identifier of the payment. |
| `total` | number |  |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/payments` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

