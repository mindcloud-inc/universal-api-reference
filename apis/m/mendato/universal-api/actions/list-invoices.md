# Mendato: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-invoices?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato invoices query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoices": {
        "edges": [
          {
            "node": {
              "cancelledAt": "2026-05-07T12:00:00.000Z",
              "completedAt": "2026-05-07T12:00:00.000Z",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "dueDate": "2026-05-07T12:00:00.000Z",
              "id": "string",
              "invoiceDate": "2026-05-07T12:00:00.000Z",
              "isNegative": true,
              "number": 1,
              "numberPrefix": "string",
              "numberSuffix": "string",
              "paidAt": "2026-05-07T12:00:00.000Z",
              "sentAt": "2026-05-07T12:00:00.000Z",
              "sentManually": true,
              "skontoApplied": true,
              "skontoEnabled": true,
              "status": "string",
              "totalAmount": 1,
              "totalNetAmount": 1,
              "type": "string"
            }
          }
        ],
        "pageInfo": {
          "endCursor": "string",
          "hasNextPage": true,
          "hasPreviousPage": true,
          "startCursor": "string"
        },
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoices.edges[].node.cancelledAt` | date |  |
| `invoices.edges[].node.completedAt` | date |  |
| `invoices.edges[].node.createdAt` | date |  |
| `invoices.edges[].node.dueDate` | date |  |
| `invoices.edges[].node.id` | string |  |
| `invoices.edges[].node.invoiceDate` | date |  |
| `invoices.edges[].node.isNegative` | boolean |  |
| `invoices.edges[].node.number` | number |  |
| `invoices.edges[].node.numberPrefix` | string |  |
| `invoices.edges[].node.numberSuffix` | string |  |
| `invoices.edges[].node.paidAt` | date |  |
| `invoices.edges[].node.sentAt` | date |  |
| `invoices.edges[].node.sentManually` | boolean |  |
| `invoices.edges[].node.skontoApplied` | boolean |  |
| `invoices.edges[].node.skontoEnabled` | boolean |  |
| `invoices.edges[].node.status` | string |  |
| `invoices.edges[].node.totalAmount` | number |  |
| `invoices.edges[].node.totalNetAmount` | number |  |
| `invoices.edges[].node.type` | string |  |
| `invoices.pageInfo.endCursor` | string |  |
| `invoices.pageInfo.hasNextPage` | boolean |  |
| `invoices.pageInfo.hasPreviousPage` | boolean |  |
| `invoices.pageInfo.startCursor` | string |  |
| `invoices.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

