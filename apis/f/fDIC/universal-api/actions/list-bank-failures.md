# FDIC: List Bank Failures

Retrieves failed bank records from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-bank-failures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-bank-failures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-bank-failures?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter for bank failure records, for example FAILYR:2023. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-delimited uppercase FDIC fields to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CERT": 1,
      "CITY": "string",
      "COST": 1,
      "FAILDATE": "string",
      "FAILYR": "string",
      "ID": "string",
      "NAME": "Ava Chen",
      "PSTALP": "string",
      "QBFASSET": 1,
      "QBFDEP": 1,
      "RESTYPE": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CERT` | number |  |
| `CITY` | string |  |
| `COST` | number |  |
| `FAILDATE` | string |  |
| `FAILYR` | string |  |
| `ID` | string |  |
| `NAME` | string |  |
| `PSTALP` | string |  |
| `QBFASSET` | number |  |
| `QBFDEP` | number |  |
| `RESTYPE` | string |  |

## Native endpoint

Through the native FDIC API, this operation is `GET /failures` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bank-failures.md) for the provider-specific parameters and requirements.

