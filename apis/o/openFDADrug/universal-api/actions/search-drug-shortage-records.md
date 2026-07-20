# openFDA Drug: Search Drug Shortage Records

Finds drug shortage records in openFDA Drug.

```
GET https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/search-drug-shortage-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openFDA Drug `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/search-drug-shortage-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/search-drug-shortage-records?${params}`, {
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
| `search` | string | no | OpenFDA search expression. |
| `limit` | number | no | Maximum records to return. Default: `5`. |
| `skip` | number | no | Number of matching records to skip. |
| `sort` | string | no | OpenFDA sort expression. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | OpenFDA response metadata including query result counts and disclaimer links. |
| `results` | array<object> | OpenFDA drug shortage records returned by the endpoint. |

## Native endpoint

Through the native openFDA Drug API, this operation is `GET /drug/shortages.json` (base URL `https://api.fda.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-drug-shortage-records.md) for the provider-specific parameters and requirements.

