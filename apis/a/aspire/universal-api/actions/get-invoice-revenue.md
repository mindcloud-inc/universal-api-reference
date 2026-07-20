# Aspire: List Invoice Revenues

Retrieves pay codes from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-invoice-revenue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-invoice-revenue?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-invoice-revenue?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "branchID": 1,
      "branchName": "Ava Chen",
      "divisionCode": "string",
      "divisionID": 1,
      "divisionName": "Ava Chen",
      "invoiceBatchID": 1,
      "invoiceDate": "string",
      "invoiceID": 1,
      "invoiceNumber": 1,
      "invoiceOpportunityID": 1,
      "invoiceRevenueID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `divisionCode` | string |  |
| `divisionID` | number |  |
| `divisionName` | string |  |
| `invoiceBatchID` | number |  |
| `invoiceDate` | string |  |
| `invoiceID` | number |  |
| `invoiceNumber` | number |  |
| `invoiceOpportunityID` | number |  |
| `invoiceRevenueID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET invoicerevenues` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-invoice-revenue.md) for the provider-specific parameters and requirements.

