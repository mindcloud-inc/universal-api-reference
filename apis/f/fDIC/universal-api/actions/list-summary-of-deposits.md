# FDIC: List Summary Of Deposits

Retrieves summary of deposits data from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-summary-of-deposits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-summary-of-deposits?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-summary-of-deposits?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter for Summary of Deposits records. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-delimited uppercase FDIC fields to include in the response. |
| `aggBy` | string | no | FDIC aggregate grouping field for Summary of Deposits data. |
| `aggSumFields` | string | no | Comma-delimited fields to sum in FDIC aggregation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ADDRESS": "string",
      "CERT": 1,
      "CITY": "string",
      "DEPDOM": 1,
      "DEPSUM": 1,
      "DEPSUMBR": 1,
      "NAME": "Ava Chen",
      "NAMEBR": "Ava Chen",
      "SIMS_LATITUDE": 1,
      "SIMS_LONGITUDE": 1,
      "STNAME": "Ava Chen",
      "YEAR": 1,
      "ZIP": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ADDRESS` | string |  |
| `CERT` | number |  |
| `CITY` | string |  |
| `DEPDOM` | number |  |
| `DEPSUM` | number |  |
| `DEPSUMBR` | number |  |
| `NAME` | string |  |
| `NAMEBR` | string |  |
| `SIMS_LATITUDE` | number |  |
| `SIMS_LONGITUDE` | number |  |
| `STNAME` | string |  |
| `YEAR` | number |  |
| `ZIP` | string |  |

## Native endpoint

Through the native FDIC API, this operation is `GET /sod` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-summary-of-deposits.md) for the provider-specific parameters and requirements.

