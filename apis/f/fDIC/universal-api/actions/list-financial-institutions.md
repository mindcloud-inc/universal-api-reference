# FDIC: List Financial Institutions

Retrieves financial institutions from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-financial-institutions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-financial-institutions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-financial-institutions?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter, for example STALP:IA AND ACTIVE:1. |
| `search` | string | no | Flexible text search against institution names, for example NAME:Island. |

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
      "ACTIVE": 1,
      "ASSET": 1,
      "CERT": 1,
      "CITY": "string",
      "DATEUPDT": "string",
      "DEP": 1,
      "NAME": "Ava Chen",
      "OFFICES": 1,
      "STALP": "string",
      "STNAME": "Ava Chen",
      "WEBADDR": "string",
      "ZIP": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ACTIVE` | number | FDIC active institution flag. |
| `ASSET` | number | Total assets. |
| `CERT` | number | FDIC certificate number. |
| `CITY` | string | Institution city. |
| `DATEUPDT` | string | Last updated date. |
| `DEP` | number | Total deposits. |
| `NAME` | string | Institution name. |
| `OFFICES` | number | Office count. |
| `STALP` | string | State abbreviation. |
| `STNAME` | string | State name. |
| `WEBADDR` | string | Institution website address. |
| `ZIP` | string | ZIP code. |

## Native endpoint

Through the native FDIC API, this operation is `GET /institutions` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-financial-institutions.md) for the provider-specific parameters and requirements.

