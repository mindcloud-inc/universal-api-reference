# FDIC: List Structure Change Events

Retrieves structure change events from FDIC.

```
GET https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-structure-change-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FDIC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-structure-change-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-structure-change-events?${params}`, {
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
| `filters` | string | no | Elastic Search query string filter for structure change events. |
| `search` | string | no | Flexible text search against history records. |

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
      "CHANGECODE": 1,
      "CLASS_TYPE_DESC": "string",
      "EFFYEAR": "string",
      "FDICREGION_DESC": "string",
      "INSTNAME": "Ava Chen",
      "PCITY": "string",
      "PROCYEAR": "string",
      "PSTALP": "string",
      "REPORT_TYPE": 1,
      "TRANSNUM": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CERT` | number |  |
| `CHANGECODE` | number |  |
| `CLASS_TYPE_DESC` | string |  |
| `EFFYEAR` | string |  |
| `FDICREGION_DESC` | string |  |
| `INSTNAME` | string |  |
| `PCITY` | string |  |
| `PROCYEAR` | string |  |
| `PSTALP` | string |  |
| `REPORT_TYPE` | number |  |
| `TRANSNUM` | number |  |

## Native endpoint

Through the native FDIC API, this operation is `GET /history` (base URL `https://api.fdic.gov/banks`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-structure-change-events.md) for the provider-specific parameters and requirements.

