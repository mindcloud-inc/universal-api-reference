# FDIC: List Institution Financials

Retrieves institution financial data from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-institution-financials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-institution-financials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-institution-financials?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter for financial records, for example CERT:3510. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-delimited uppercase FDIC fields to include in the response. |
| `aggBy` | string | no | FDIC aggregate grouping field for financial data. |
| `aggSumFields` | string | no | Comma-delimited fields to sum in FDIC aggregation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ASSET": 1,
      "CERT": 1,
      "DEP": 1,
      "DEPDOM": 1,
      "NAME": "Ava Chen",
      "NETINC": 1,
      "REPDTE": "string",
      "ROA": 1,
      "ROE": 1,
      "STALP": "string",
      "STNAME": "Ava Chen",
      "ZIP": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ASSET` | number | Total assets. |
| `CERT` | number | FDIC certificate number. |
| `DEP` | number | Total deposits. |
| `DEPDOM` | number | Domestic deposits. |
| `NAME` | string | Institution name. |
| `NETINC` | number | Net income. |
| `REPDTE` | string | Report date. |
| `ROA` | number | Return on assets. |
| `ROE` | number | Return on equity. |
| `STALP` | string | State abbreviation. |
| `STNAME` | string | State name. |
| `ZIP` | number | ZIP code. |

## Native endpoint

Through the native FDIC API, this operation is `GET /financials` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-institution-financials.md) for the provider-specific parameters and requirements.

