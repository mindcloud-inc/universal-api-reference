# OpenFDA: Search Tobacco Problem Records

Finds tobacco problem records in OpenFDA.

```
GET https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/search-tobacco-problem-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFDA `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/search-tobacco-problem-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFDA/latest/actions/search-tobacco-problem-records?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `results` | array<object> | OpenFDA records returned by the dataset endpoint. |

## Native endpoint

Through the native OpenFDA API, this operation is `GET /tobacco/problem.json` (base URL `https://api.fda.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tobacco-problem-records.md) for the provider-specific parameters and requirements.

