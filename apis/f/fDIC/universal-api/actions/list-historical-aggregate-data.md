# FDIC: List Historical Aggregate Data

Retrieves historical aggregate banking data from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-historical-aggregate-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-historical-aggregate-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-historical-aggregate-data?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter for historical aggregate data. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-delimited uppercase FDIC fields to include in the response. |
| `aggBy` | string | no | FDIC aggregate grouping field for summary data. |
| `aggSumFields` | string | no | Comma-delimited fields to sum in FDIC aggregation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ASSET": 1,
      "BANKS": 1,
      "DEP": 1,
      "EQ": 1,
      "LNLS": 1,
      "NETINC": 1,
      "ROA": 1,
      "ROE": 1,
      "STNAME": "Ava Chen",
      "TOTAL": 1,
      "YEAR": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ASSET` | number |  |
| `BANKS` | number |  |
| `DEP` | number |  |
| `EQ` | number |  |
| `LNLS` | number |  |
| `NETINC` | number |  |
| `ROA` | number |  |
| `ROE` | number |  |
| `STNAME` | string |  |
| `TOTAL` | number |  |
| `YEAR` | string |  |

## Native endpoint

Through the native FDIC API, this operation is `GET /summary` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-historical-aggregate-data.md) for the provider-specific parameters and requirements.

