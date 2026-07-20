# SalesRender: Get Company

Retrieves company details from SalesRender.

```
GET https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/get-company?connectionId=$CONNECTION_ID&query=query%20%7B%20company%20%7B%20id%20name%20createdAt%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { company { id name createdAt } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/get-company?${params}`, {
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
| `query` | string | yes | GraphQL query document to send to the SalesRender CRM API. Default: `query {\n  company {\n    id\n    name\n    createdAt\n  }\n}`. Example: `query { company { id name createdAt } }`. |

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
        "company": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen"
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
| `data.company.createdAt` | date | Company creation timestamp. |
| `data.company.id` | string | SalesRender company ID. |
| `data.company.name` | string | SalesRender company name. |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

