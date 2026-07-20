# SalesRender: List Customers

Retrieves customers from SalesRender.

```
GET https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-customers?connectionId=$CONNECTION_ID&query=query%20%7B%20customersFetcher%20%7B%20customers%20%7B%20id%20email%20registeredAt%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { customersFetcher { customers { id email registeredAt } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-customers?${params}`, {
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
| `query` | string | yes | GraphQL query to execute against SalesRender. Default: `query {\n  customersFetcher {\n    customers {\n      id\n      email\n      registeredAt\n    }\n  }\n}`. Example: `query { customersFetcher { customers { id email registeredAt } } }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional GraphQL variables object. Default: `{}`. Example: `Optional JSON variables string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "customersFetcher": {
          "customers": [
            {
              "email": "ava@example.com",
              "id": "string",
              "registeredAt": "2026-05-07T12:00:00.000Z"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.customersFetcher.customers[].email` | string | Customer email address. |
| `data.customersFetcher.customers[].id` | string | Customer ID. |
| `data.customersFetcher.customers[].registeredAt` | date | Customer registration timestamp. |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

