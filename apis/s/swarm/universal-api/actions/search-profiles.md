# Swarm: Search Profiles

Finds profiles in Swarm using an OpenSearch query.

```
GET https://connect.mindcloud.co/v1/universal/swarm/latest/actions/search-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swarm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swarm/latest/actions/search-profiles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swarm/latest/actions/search-profiles?${params}`, {
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
      "ids": [
        "string"
      ],
      "paginationToken": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ids` | array<string> | Matching Swarm profile IDs. |
| `paginationToken` | string | Cursor token for the next page. |
| `totalCount` | number | Total number of matching profiles. |

## Native endpoint

Through the native Swarm API, this operation is `POST /v2/profiles/search` (base URL `https://bee.theswarm.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-profiles.md) for the provider-specific parameters and requirements.

