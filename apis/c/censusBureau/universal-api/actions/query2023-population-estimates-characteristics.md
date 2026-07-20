# Census Bureau: Query 2023 Population Estimates Characteristics

Queries Census Bureau 2023 population estimates characteristics.

```
GET https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2023-population-estimates-characteristics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Census Bureau `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2023-population-estimates-characteristics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2023-population-estimates-characteristics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Census Bureau API returns.

## Native endpoint

Through the native Census Bureau API, this operation is `GET /2023/pep/charv` (base URL `https://api.census.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query2023-population-estimates-characteristics.md) for the provider-specific parameters and requirements.

