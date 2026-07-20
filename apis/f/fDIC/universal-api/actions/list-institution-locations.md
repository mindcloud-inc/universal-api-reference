# FDIC: List Institution Locations

Retrieves institution locations from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-institution-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-institution-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-institution-locations?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter for location records, for example STALP:IA. |

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
      "ADDRESS": "string",
      "CERT": "string",
      "CITY": "string",
      "ID": "string",
      "LATITUDE": 1,
      "LONGITUDE": 1,
      "MAINOFF": 1,
      "NAME": "Ava Chen",
      "OFFNAME": "Ava Chen",
      "STALP": "string",
      "STNAME": "Ava Chen",
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
| `CERT` | string |  |
| `CITY` | string |  |
| `ID` | string |  |
| `LATITUDE` | number |  |
| `LONGITUDE` | number |  |
| `MAINOFF` | number |  |
| `NAME` | string |  |
| `OFFNAME` | string |  |
| `STALP` | string |  |
| `STNAME` | string |  |
| `ZIP` | string |  |

## Native endpoint

Through the native FDIC API, this operation is `GET /locations` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-institution-locations.md) for the provider-specific parameters and requirements.

