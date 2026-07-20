# Census Bureau: Query 2024 ACS 5-Year Data Profiles

Queries Census Bureau 2024 ACS 5-Year data profiles.

```
GET https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2024-acs5-data-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Census Bureau `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2024-acs5-data-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/censusBureau/latest/actions/query2024-acs5-data-profiles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Census Bureau API returns.

## Native endpoint

Through the native Census Bureau API, this operation is `GET /2024/acs/acs5/profile` (base URL `https://api.census.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query2024-acs5-data-profiles.md) for the provider-specific parameters and requirements.

