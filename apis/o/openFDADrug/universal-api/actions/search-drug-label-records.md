# openFDA Drug: Search Drug Label Records

Finds drug label records in openFDA Drug.

```
GET https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/search-drug-label-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a openFDA Drug `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/search-drug-label-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFDADrug/latest/actions/search-drug-label-records?${params}`, {
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
| `search` | string | no | OpenFDA search expression, such as drug_interactions:caffeine. |
| `limit` | number | no | Maximum records to return. OpenFDA allows up to 1000 for this endpoint. Default: `5`. |
| `skip` | number | no | Number of matching records to skip. OpenFDA supports skip values up to 25000. |
| `sort` | string | no | OpenFDA sort expression, such as effective_time:desc. |

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
| `results` | array<object> | OpenFDA structured product labeling records returned by the endpoint. |

## Native endpoint

Through the native openFDA Drug API, this operation is `GET /drug/label.json` (base URL `https://api.fda.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-drug-label-records.md) for the provider-specific parameters and requirements.

