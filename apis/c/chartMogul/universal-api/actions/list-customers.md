# ChartMogul: List Customers

Retrieves customers from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-customers?${params}`, {
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
| `dataSourceUuid` | string | no | Filter customers by data source UUID. |
| `email` | string | no | Search for customers by email address. |
| `externalId` | string | no | Filter by the customer external identifier. |
| `status` | string | no | Filter by customer status. |
| `system` | string | no | Filter by billing system type. |
| `withAssociatedEmails` | boolean | no | Include customers linked through associated contact email addresses. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arr": 1,
      "city": "string",
      "company": "string",
      "country": "string",
      "currency": "string",
      "customerSince": "2026-05-07T12:00:00.000Z",
      "dataSourceUuid": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "id": 1,
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "mrr": 1,
      "name": "Ava Chen",
      "state": "string",
      "status": "string",
      "uuid": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arr` | number |  |
| `city` | string |  |
| `company` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `customerSince` | date |  |
| `dataSourceUuid` | string |  |
| `email` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `lastSeen` | date |  |
| `mrr` | number |  |
| `name` | string |  |
| `state` | string |  |
| `status` | string |  |
| `uuid` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /customers` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

